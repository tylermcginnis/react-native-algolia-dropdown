# react-native-algolia-dropdown
This component is rad. I just haven't had time to document it. If you're using Algolia with React Native and you need an Instagram-ish search bar (with dropdown results), hit me up on Twitter and I'll walk you through it. @tylermcginnis33

##Example
```
<AlgoliaDropdown
  appID={algoliaConfig.APP_ID}
  style={{backgroundColor: colors.tabPrimary, borderBottomWidth: 1, borderColor: colors.border, paddingTop: Platform.OS === 'ios' ? 25 : 0}}
  footerHeight={64}
  sideComponent={<Filter onPress={this.handleFilterPress} width={this.state.filterWidth} />}
  apiKey={algoliaConfig.SEARCH_API}>
    <UserPreview
      index='users'
      title='People'
      params={{hitsPerPage: 3}}
      onToProfile={(userId) => this.handleToProfile(userId)}
      small={true} />
    <PostSearchContainer
      navigator={this.props.navigator}
      index='posts'
      title='Public Posts'
      params={{hitsPerPage: 3}} />
</AlgoliaDropdown>
```

#### Renders this
![React Native Algolia Dropdown](https://cloud.githubusercontent.com/assets/2933430/17902287/ed5ad2f2-6923-11e6-9ca1-3dbdae5e74e8.gif)
