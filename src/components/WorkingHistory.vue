<template>
    <div class="container mx-auto">
        <div class="mt-10 mb-10">
            <div class="text-center text-3xl font-semibold text-sky-800">Working History</div>
        </div>
        <div v-for="job in workingHistory">
            <WorkCard :job="job" />
        </div>
        
    </div>
</template>
<script>
import WorkCard from './WorkCard.vue';
import usFlag from '../assets/flagus.svg'
import auFlag from '../assets/flagaustralia.svg'
import clFlag from '../assets/flagchile.svg'
export default {
    components: {
        WorkCard
    },
    data() {
        return {
            workingHistory: [{
                company: "Pitchtape",
                location: "New York, USA",
                flag: usFlag,
                startDate: "Jan 2023",
                endDate: "Now",
                title: "VP Of Engineering",
                description: `As an accomplished VP of Engineering, I architected, designed, and developed the innovative pitchtape platform for both enterprise and consumer products. 
                I managed the entire product lifecycle, from planning to releasing features, and collaborated with various departments throughout the company to ensure alignment with business goals and requirements. 
                During my tenure, I was responsible for transforming ideas into actionable features, prioritizing development efforts, and conducting design reviews to maintain a high level of quality across the platform. 
                Through my leadership and technical expertise, I was able to successfully deliver multiple feature releases on time and within budget. 
                Moreover, I actively participated in code reviews, continuous integration and delivery, and agile development practices to ensure the platform was scalable, robust, and reliable. 
                My ability to communicate technical concepts effectively to both technical and non-technical stakeholders contributed to the overall success of the platform.`
            },{
                company: "Pitchtape",
                location: "New York, USA",
                flag: usFlag,
                startDate: "Dic 2020",
                endDate: "Dic 2022",
                title: "Lead Senior Software Engineer",
                description: `
                As a software developer, I successfully implemented a new version of the software, including Back-end, DevOps, and Front-end components. I also created a Kubernetes Helm recipe, which made installation and maintenance of the product easier in the cloud environment. 
                During the project, I identified video processing time as a bottleneck, and I reduced encoding times by approximately 60% while also decreasing the CPU usage overhead by about 60%. I made better use of existing resources, code base, and technologies to achieve these improvements. 
                I migrated the existing Kubernetes and CI pipelines to reduce pipeline times and improve security by utilizing Kubernetes secrets. As part of the project, I documented, analyzed, and reviewed the system usage, metrics, and costs associated with the product. I also developed a new (beta) version of the video service, which reduced processing times from minutes to just a few seconds. The new version was developed using Python FastAPI and PythonRQ, resulting in reduced workload and processing a considerable amount, leading to reduced costs and allowing parallel scaling on the platform into huge increases. 
                In addition, I successfully led, managed, and planned with other developers in the team.
                I also designed, reviewed, and implemented architecture changes that added value to the product and helped in the company roadmap.
                `
            },{
                company: "Teller Finance",
                location: "San Francisco, California, USA",
                flag: usFlag,
                startDate: "Mar 2020",
                endDate: "Nov 2020",
                title: "Back-end Cloud Engineer",
                description: `
                As a software engineer at Teller, I was responsible for designing, modeling, and developing the project while also contributing to the back-end and cloud implementation. 
                I created and maintained a JSON RPC NodeJS API service that handled web3 transactions, ensuring smooth and efficient operations. 
                To optimize the deployment process, I created, maintained, and improved docker recipes and setups, including ECR & EKS implementation. Additionally, I designed a helm recipe for setting up a node in the distributed system architecture, which allowed for easy cluster installation and distribution. 
                To achieve the goal of auto-upgrading components for each micro-service, I designed a system architecture that used helm and flux, with git repo-based configuration. This approach ensured that components were always up-to-date and that the system operated efficiently. I also reviewed code, unit tests, and documentation of the RPC methods to ensure their effectiveness and accuracy. 
                Furthermore, I developed and set up CI/CD integrations with Github actions, using docker, kubectl, and helm, which ensured that the product was delivered to customers quickly and efficiently.
                `
            },{
                company: "Goldi",
                flag: usFlag,
                location: "New York, USA",
                startDate: "Mar 2019",
                endDate: "Dic 2020",
                title: "Senior Back-end Developer",
                description: `
                As a Python Developer, I developed and maintained a micro-service oriented Django API service that handled video content with encoding tasks using a queue in RabbitMQ. I used Python and Celery to create efficient and scalable services that met the needs of the project. 
                To improve the efficiency of the project, I created, maintained, and improved Docker recipes, Docker setup, and Kubernetes implementation. This made the deployment process more streamlined, and improved the overall reliability of the system. 
                In addition, I set up and developed CI/CD integrations with GitLab using Docker and Kubernetes. This made it easy for the team to build, test, and deploy new code changes, ensuring that the system was always up-to-date. 
                To ensure the smooth operation of the system, I configured, monitored, and maintained DevOps services, including Redis, PostgreSQL, and Redis, both in standalone and Kubernetes instances. This allowed me to quickly identify and resolve any issues that arose. 
                Finally, I reviewed code, unit tests, and documentation, ensuring that the team was following best practices and maintaining high code quality.
                `
            },{
                company: "Stitch",
                location: "Sydney, Australia",
                flag: auFlag,
                startDate: "Jan 2019",
                endDate: "Feb 2019",
                title: "Back-end Developer",
                description: `
                As a software engineer, I had the opportunity to work on improving an existing product. One of my responsibilities was to review the product and technologies used, and then create a list of features that could be improved. Based on this list, I implemented several enhancements to the product, including: 
                Implementing authentication rate limiting to block brute force attempts. 
                Setting up a Docker environment to streamline the deployment process. 
                Implementing a cache system using Amazon Elastic Cache to improve performance. 
                Writing feature and specification tests using BDD/unittest to increase test coverage. 
                
                In addition to these technical tasks, I also worked collaboratively with the rest of the team to contribute to several features that improved the product. Overall, this experience allowed me to apply my skills in software development and problem-solving to make meaningful contributions to a product and work effectively with a team.
                Finally, I reviewed code, unit tests, and documentation, ensuring that the team was following best practices and maintaining high code quality.
                `
            },{
                company: "Goldi",
                location: "New York, USA",
                flag: usFlag,
                startDate: "Jan 2017",
                endDate: "Dec 2018",
                title: "Back-end Team Leader",
                description: `
                As the lead developer for a media content API, I developed and maintained the system using Python, Django, and the Rest Framework, along with Celery, RabbitMQ, and other technologies like Docker, Fabric, Gunicorn, and HAProxy. 
                Working in a micro-service architecture, I utilized message queues and tasks to ensure efficient communication between services. I also contributed to the overall system architecture, tools, and libraries to improve the product. 
                As a team leader, I guided and directed the development team to achieve planning goals alongside the product manager and CTO. Additionally, I provided regular reports on the team's status to company stakeholders. 
                My responsibilities also included reviewing, merging, and deploying code to various environments using the latest technologies. 
                Throughout my work, I encountered and solved many problems and challenges, always making sure to keep things moving forward. 
                This position required me to work within a multicultural and dynamic team in a fast-paced NYC startup environment.
                `
            },{
                company: "Analyze",
                location: "Santiago, Chile",
                flag: clFlag,
                startDate: "Dec 2014",
                endDate: "Jan 2017",
                title: "Full-Stack Team Leader",
                description: `
                Developed and implemented various tools and technologies to monitor the status of web crawlers, ensuring efficient and effective data extraction from flash sites. 
                Led the development of an enterprise software for a company from the ground up, including architecting and modeling the system, and setting coding standards and development tools. 
                Effectively managed a team of developers, providing guidance and support to ensure timely and high-quality delivery of projects. 
                Played a key role in recruiting, training, and mentoring new team members, ensuring a high-performing and collaborative team culture. 
                Proactively planned and tracked project timelines, milestones, and budgets, optimizing resource allocation and ensuring project success. 
                Worked closely with stakeholders to understand business requirements and develop effective solutions that meet their needs.
                `
            },{
                company: "AlfaOmega",
                location: "Chillán, Chile",
                flag: clFlag,
                startDate: "Nov 2014",
                endDate: "Dec 2014",
                title: "Software Engineer",
                description: `
                Developed a real-time application for a hospital nurse call system, using a Programmable Logic Controller (PLC) to handle and configure real-time alerts. 
                Implemented the project for the hospital of Chillán, where it remains in use to this day, ensuring effective and efficient communication between patients and nurses. 
                Leveraged Node.js and JavaScript, utilizing the node-webkit library to create a desktop application that provided seamless integration and functionality. 
                Conducted thorough testing and troubleshooting, identifying and resolving issues in a timely and efficient manner to ensure optimal performance. 
                Collaborated closely with hospital staff and stakeholders to gather requirements and feedback, ensuring the application met the unique needs of the hospital and its patients. 
                Provided ongoing support and maintenance to ensure the continued success and usability of the application.
                `
            },{
                company: "Foris.ia",
                location: "Santiago, Chile",
                flag: clFlag,
                startDate: "Sep 2012",
                endDate: "Dec 2013",
                title: "Lead Engineer",
                description: `
                As a Lead Engineer, I developed and maintained a product using CakePHP, which included implementing new features, fixing bugs, and ensuring high code quality. I also initiated a company-wide migration from CakePHP to Django and introduced Python as the primary language for web development. 
                Additionally, I played a key role in creating a new analytics area for the company, where I planned, tracked, and managed a team of developers. As part of this initiative, I created a cutting-edge analytics platform called REAL, which was based on job post historical records from trabajando.com. The platform was designed to be user-friendly and provided valuable insights for both end-users and companies. I utilized statistical models written in R to create advanced analytics capabilities and integrated the platform with Django. The data visualizations were rendered using Highcharts. 
                In addition to REAL, I also created Retention Manager, a software solution that helped universities identify potential drop-out students and prevent them from leaving. This involved designing and developing the application from scratch and incorporating machine learning algorithms to predict student behavior patterns. 
                Overall, my contributions to the company have helped drive innovation and improve their overall performance.
                `
            }]
        }
    }
}
</script>
