<template>
    <div class="container mx-auto">
        <div class="my-10 inline">
            <div class="text-center text-3xl font-semibold text-cyan-700">Technologies</div>
        </div>
        <div class="my-10 relative bg-neutral-100 p-3 align-top inline-block mx-5">
            <div class="text-left text-2xl font-semibold text-cyan-800 my-2"> Back-end </div>
            <ul class="list-disc ml-10 my-1" v-for="tech in backend">
                <TechnologyPoint :tech="tech" />
            </ul>
        </div>
        <div class="my-10 relative bg-neutral-100 p-3 align-top inline-block mx-5">
            <div class="text-left text-2xl font-semibold text-cyan-800 my-2"> Front-end </div>
            <ul class="list-disc ml-10 my-1" v-for="tech in frontend">
                <TechnologyPoint :tech="tech" />
            </ul>
        </div>
        <div class="my-10 relative bg-neutral-100 p-3 align-top inline-block mx-5">
            <div class="text-left text-2xl font-semibold text-cyan-800 my-2"> Cloud Services </div>
            <ul class="list-disc ml-10 my-1" v-for="tech in cloud">
                <TechnologyPoint :tech="tech" />
            </ul>
        </div>
        <div class="my-10 relative bg-neutral-100 p-3 align-top inline-block mx-5">
            <div class="text-left text-2xl font-semibold text-cyan-800 my-2"> DevOps </div>
            <ul class="list-disc ml-10 my-1" v-for="tech in devops">
                <TechnologyPoint :tech="tech" />
            </ul>
        </div>
        
    </div>
</template>
<script>
import TechnologyPoint from './TechnologyPoint.vue';
import pythonLogo from '../assets/python.svg'
import djangoLogo from '../assets/django.svg'
import jsonLogo from '../assets/json.svg'
import graphqlLogo from '../assets/graphql.svg'
import fastAPILogo from '../assets/fastapi.svg'
import pytestLogo from '../assets/pytest.png'
import gitLogo from '../assets/git.svg'
import nodeLogo from '../assets/nodejsv2.svg'
import ffmpegLogo from '../assets/ffmpeg.svg'
import javascriptLogo from '../assets/javascript.svg'
import vueLogo from '../assets/vue.svg'
import reactLogo from '../assets/react.svg'
import css3Logo from '../assets/css3.svg'
import html5Logo from '../assets/html5.svg'
import bootstrapLogo from '../assets/bootstrap.svg'
import tailwindLogo from '../assets/tailwind.svg'
import jestLogo from '../assets/jest.svg'
import mochaLogo from '../assets/mocha.svg'
import webrtcLogo from '../assets/webrtc.svg'
import kubernetesLogo from '../assets/kubernetes.svg'
import helmLogo from '../assets/helm.svg'
import googlecloudLogo from '../assets/googlecloud.svg'
import awsLogo from '../assets/aws.svg'
import digitaloceanLogo from '../assets/digitalocean.svg'
import dockerLogo from '../assets/docker.svg'
import githubLogo from '../assets/github.svg'
import githubactionsLogo from '../assets/githubactions.svg'
import gitlabLogo from '../assets/gitlab.svg'
import gitlabciLogo from '../assets/gitlabci.svg'
import newrelicLogo from '../assets/newrelic.svg'
import datadogLogo from '../assets/datadog.svg'
import logstashLogo from '../assets/logstash.svg'
import sentryLogo from '../assets/sentry.svg'
import postgresqlLogo from '../assets/postgresql.svg'
import redisLogo from '../assets/redis.svg'
import prometheusLogo from '../assets/prometheus.svg'
import grafanaLogo from '../assets/grafana.svg'
import elasticLogo from '../assets/elastic.svg'
import fluxcdLogo from '../assets/fluxcd.png'
import veleroLogo from '../assets/velero.png'

export default {
    components : {
        TechnologyPoint
    },
    data() {
        return {
            backend: [
                { name: "Python", logo: pythonLogo, url: "https://www.python.org/"},
                { name: "Django", logo: djangoLogo, url: "https://www.djangoproject.com/" },
                { name: "Django Rest Framework", logo: jsonLogo, url: "https://www.django-rest-framework.org/" },
                { name: "Graphene", logo: graphqlLogo, url: "https://graphene-python.org/" },
                { name: "FastAPI", logo: fastAPILogo, url: "https://fastapi.tiangolo.com/" },
                { name: "Pytest", logo: pytestLogo, url: "https://pytest.org/" },
                { name: "Git", logo: gitLogo, url: "https://github.com/git/git" },
                { name: "NodeJS", logo: nodeLogo, url: "https://nodejs.org/en" },
                { name: "FFmpeg", logo: ffmpegLogo, url: "https://ffmpeg.org/" }
            ],
            frontend: [
                { name: "Javascript", logo: javascriptLogo, url: "https://developer.mozilla.org/en-US/docs/Web/JavaScript" },
                { name: "VueJS", logo: vueLogo, url: "https://vuejs.org/" },
                { name: "React", logo: reactLogo, url: "https://es.reactjs.org/" },
                { name: "CSS3", logo: css3Logo, url: "https://www.w3.org/Style/CSS/Overview.en.html" },
                { name: "HTML5", logo: html5Logo, url: "https://html5.org/" },
                { name: "Bootstrap", logo: bootstrapLogo, url: "https://getbootstrap.com/" },
                { name: "TailwindCSS", logo: tailwindLogo, url: "https://tailwindcss.com/" },
                { name: "Jest", logo: jestLogo, url: "https://jestjs.io/" },
                { name: "Mocha", logo: mochaLogo, url: "https://mochajs.org/" },
                { name: "WebRTC", logo: webrtcLogo, url: "https://webrtc.org/" }
            ],
            cloud : [
                { name: "Google Cloud Services (GCS)", logo: googlecloudLogo, url: "https://cloud.google.com/" },
                { name: "Amazon Web Services (AWS)", logo: awsLogo, url: "https://aws.amazon.com/" },
                { name: "Digital Ocean Cloud", logo: digitaloceanLogo, url: "https://www.digitalocean.com/" }
            ],
            devops: [
                { name: "Kubernetes", logo: kubernetesLogo, url: "https://kubernetes.io/" },
                { name: "Helm", logo: helmLogo, url: "https://helm.sh/" },
                { name: "Docker", logo: dockerLogo, url: "https://www.docker.com/" },
                { name: "Github", logo: githubLogo, url: "https://github.com/" },
                { name: "Github Actions", logo: githubactionsLogo, url: "https://github.com/features/actions" },
                { name: "GitLab", logo: gitlabLogo, url: "https://about.gitlab.com/" },
                { name: "GitLab CI/CD", logo: gitlabciLogo, url: "https://docs.gitlab.com/ee/ci/" },
                { name: "New Relic", logo: newrelicLogo, url: "https://newrelic.com/" },
                { name: "DataDog", logo: datadogLogo, url: "https://www.datadoghq.com/" },
                { name: "LogStash", logo: logstashLogo, url: "https://www.elastic.co/logstash/" },
                { name: "Sentry", logo: sentryLogo, url: "https://sentry.io/" },
                { name: "PostgreSQL", logo: postgresqlLogo, url: "https://www.postgresql.org/" },
                { name: "Redis", logo: redisLogo, url: "https://redis.io/" },
                { name: "Prometheus", logo: prometheusLogo, url: "https://prometheus.io/" },
                { name: "Grafana", logo: grafanaLogo, url: "https://grafana.com/" },
                { name: "Elastic Search", logo: elasticLogo, url: "https://www.elastic.co/" },
                { name: "Flux", logo: fluxcdLogo, url: "https://fluxcd.io/" },
                { name: "Velero", logo: veleroLogo, url: "https://github.com/vmware-tanzu/velero" },
            ]
        }
    }
}
</script>
