# amuse-test

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Q&A

> > 1. React 나 기타 JS framework 의 경험이 있다면, 에서 상태관리를 어떻게 하였으며, 해당 상태관리의 장점과 단점은 무엇인가요? (예, immutable 상태관리)
> >    > React를 사용했었습니다. 부트캠프에서 2주, 4주 프로젝트에서 사용을 했었고, 로로젬 회사에서 사용을 했었습니다.
> >    > 상태관리를 immutable과 Redux를 활용해서 관리를 했습니다.
> >    > Redux는 상태관리를 한곳에서 하기 때문에 유지보수에 용이 했지만, 초기 셋팅이 복잡한 단점이 있습니다. 규모가 큰 경우에는 용이하지만, 작은 규모는 오히려 코드를 복잡하게 만듭니다.
> >    > immutable은 용어 그대로 객체의 불변성을 유지합니다. React나 Redux에서 상태관리를 할 때, 불필요한 렌더링을 줄이고, 필요한 부분만 수정하면서 state 값을 불변의 상태로 유지하면서 변경 해줍니다. immutable.js에서 기본적으로 제공하는 method들이 많기 때문에 필요한 부분만 수정하기 용이 합니다. 하지만, 코드를 작성할 때, 항상 상태값을 불러올 때, method를 사용해야 한다는 단점이 있습니다.

> > 2.Docker 를 사용한 경험이 있다면, 해당 use case 를 간단히 설명해 주세요.
> >
> > > Docker를 사용한 경험은 없습니다. 그렇지만 docker를 사용하면 server나 db쪽 setting 할때, 용이한 도구라고 들었습니다.
