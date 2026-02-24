---
hide:
  - feedback
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amazon Bedrock Recipes</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* Reset and base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: #333333; /* Light Black */
            background-color: #ffffff; /* White */
        }
        /* Hero section */
        .hero {
            background: linear-gradient(135deg, #2c3e50, #34495e, #95a5a6);
            color: #ffffff; /* White */
            text-align: center;
            padding: 1rem 1rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            overflow: hidden;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.15) 10%, transparent 38%),
                        radial-gradient(circle, rgba(255,255,255,0.15) 10%, transparent 30%);
            background-position: 0 0, 50px 50px;
            background-size: 100px 100px;
            opacity: 0.3;
            animation: moveBackground 3s linear infinite;
            z-index: 1;
        }
        @keyframes moveBackground {
            0% { transform: translate(0, 0); }
            100% { transform: translate(-50px, -50px); }
        }
        .hero-content img {
            max-width: 155px; /* Reduced from 200px */
            margin-right: 1rem;
            vertical-align: middle;
        }
        .hero-content h1 {
            font-size: 3rem; /* Reduced from 3rem */
            font-weight: 700;
            color: #ffffff;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            display: inline-block;
            vertical-align: middle;
            margin: 0;
        }
        .hero p {
            font-size: 1.1rem; /* Reduced from 1.2rem */
            margin-bottom: 1.5rem; /* Reduced from 2rem */
            max-width: 500px; /* Reduced from 600px */
            margin-left: auto;
            margin-right: auto;
        }
        .btn {
            display: inline-block;
            padding: 10px 20px; /* Reduced from 12px 24px */
            background-color: #333333; /* Light Black */
            color: #ffffff; /* White */
            text-decoration: none;
            border-radius: 4px;
            transition: all 0.3s ease-in-out;
            font-weight: 500;
            position: relative;
            z-index: 2;
        }
        .btn:hover {
            background-color: #000000; /* Black */
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            transform: translateY(-2px);
        }
        .btn:link, .btn:visited, .btn:hover, .btn:active {
            color: #ffffff; /* White */
            text-decoration: none;
        }
        /* Main content */
        h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: #333333; /* Light Black */
        }
        /* Features section */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }
        .card {
            background-color: #f7f7f7; /* Light Grey */
            border-radius: 8px;
            padding: 10px;
            transition: box-shadow 0.2s ease-in-out;
        }
        .card:hover {
            box-shadow: 0 0 30px rgba(0, 0, 0, 0.3);
        }
        .card h3 {
            font-size: 1rem;
            margin-bottom: 1rem;
            color: #333333; /* Light Black */
        }
        .card p {
            margin-bottom: 1rem;
            color: #555555; /* Light Black */
        }
        .button {
            display: inline-block;
            background-color: #333333; /* Light Black */
            color: #ffffff; /* White */
            padding: 0.5rem 1rem;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        .button:hover {
            background-color: #000000; /* Black */
        }
        pre {
            background-color: #f2f2f2; /* Lightest Grey */
            padding: 1rem;
            border-radius: 5px;
            overflow-x: auto;
        }
        code {
            font-family: 'Roboto Mono', monospace;
        }
        .grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 10px;
        }
        .grid-item {
            background: #f5f5f5;
            padding: 10px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
    <div class="hero">
        <div class="hero-content">
            <img src="bedrock_logo.png" alt="Amazon Bedrock Logo">
            <h1>Amazon Bedrock Cookbook</h1>
        </div>
    </div>

    <main>
        <section id="getting-started" class="features">
            <h2>Getting Started</h2>
            <div class="card">
                <p>In this section, we will show you how to get started with Amazon Bedrock within a few minutes. We will use the OpenAI-compatible APIs: Responses and Chat Completions API, and the Bedrock SDK APIs: Invoke and Converse API to show you how to run an inference request.</p>
                
                <h3>Step 1 - AWS Account</h3>
                <p>If you have an AWS account already, skip this step and go to step 2. If you are new to AWS, <a href="https://aws.amazon.com/free/" target="_blank">sign up for an AWS account</a> and follow instructions.</p>
                
                <h3>Step 2 - API Key</h3>
                <p>Once you have an AWS account, you can create a long-term API key to authenticate your requests to Amazon Bedrock. To do that, go to the Amazon Bedrock service in AWS Console and generate a long term key. For more information, see the <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/api-keys.html" target="_blank">API keys section</a> in the Build chapter.</p>
                
                <h3>Step 3 - Get the SDK</h3>
                <p>To use this getting started guide, you must have Python already installed. Then install the relevant software depending on the APIs you are using.</p>
            </div>
                <div class="card">
                    <h3>Using Native Bedrock APIs (Invoke & Converse)</h3>
                    <pre><code># Install AWS Python SDK
pip install boto3
                    <h3>Using Open API compatible APIs (Responses & Chat Completions)</h3>
                    <pre><code># Install AWS Python SDK
pip install boto3 openai

# Clone the repository and use available notebooks
git clone https://github.com/aws-samples/amazon-bedrock-samples.git
cd amazon-bedrock-samples</code></pre>
                </div>
        </section>

        <section class="features">
            <h2>Features</h2>
            <div class="grid">
                <div class="card">
                    <h3>Models</h3>
                    <p>With access to hundreds of top foundation models (FMs) to power your applications and the ability to swap them in and out without rewriting code, Amazon Bedrock gives you the flexibility to build and innovate as your needs evolve.</p>
                    <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/models.html" target="_blank">Learn More</a>
                </div>
                <div class="card">
                    <h3>Build with Amazon Bedrock</h3>
                    <p>To start building models using Amazon Bedrock, first, start from your use-case. Then choose an API, an endpoint, and then start using the models programmatically.</p>
                    <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/build.html" target="_blank">Learn More</a>
                </div>
                <div class="card">
                    <h3>Model Customization</h3>
                    <p>You can customize Amazon Bedrock foundation models in order to improve their performance and create a better customer experience.</p>
                    <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/custom-models.html" target="_blank">Learn More</a>
                </div>
                <div class="card">
                    <h3>Security, Guardrails and Observability</h3>
                    <p>Security in Amazon Bedrock encompasses multiple layers of protection for your data, applications, and infrastructure.
                    Amazon Bedrock Guardrails offer control mechanisms to ensure AI outputs align with organizational policies and ethical standards. Observability in Amazon Bedrock helps you track performance, manage resources, and automate deployments.
                    </p>
                    <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/security.html" target="_blank">Learn More</a>
                </div>
                <div class="card">
                    <h3>Capacity, Limits and Cost optimization </h3>
                    <p>Amazon Bedrock offers flexible capacity options to match your workload requirements and budget. Understanding the differences between on-demand tiers (Flex, Priority, Standard), reserved tier, batch processing, and cross-region inference helps you optimize both performance and cost.</p>
                    <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/capacity-limits-cost-optimization.html" target="_blank">Learn More</a>
                </div>
                <div class="card">
                    <h3>Additional Capabilities</h3>
                    <p>Additionally, Amazon Bedrock provides advanced capabilities like transforming unstructured data into meaningful insights, building knowledge bases with your data, evaluate models and knowledge bases and build end to end generative AI workflows to enhance your generative AI application.</p>
                    <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/capacity-limits-cost-optimization.html" target="_blank">Learn More</a>
                </div>
                <div class="card">
                    <h3>Code Samples</h3>
                    <p>The following section shows how to use Amazon Bedrock with an AWS softeare development toolkit (SDK).</p>
                    <a href="https://docs.aws.amazon.com/bedrock/latest/userguide/service_code_examples.html" target="_blank">Learn More</a>
                </div>
            </div>
        </section>
    </main>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>