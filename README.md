# Shoulda-Kept-Assign-To
By [Tinfoil Security](http://tinfoilsecurity.com/)

Shoulda-matchers, ([official Git repo](https://github.com/thoughtbot/shoulda-matchers)), removed the respond_with_content_type matcher in version 2.0.0. We missed it dearly, enough to bring it back. This gem includes all of the current version of shoulda-matchers, and it adds the 'respond_with_content_type' matcher back in, just the way it was before it was mercilessly destroyed.

## Example (from shoulda-matchers, v1.5)

```ruby
describe PostsController, "#show" do
  it { should permit(:title, :body).for(:create) }

  context "for a fictional user" do
    before do
      get :show, :id => 1
    end

    it { should respond_with_content_type(:json) }
  end
end
```

## Installation

In Rails 3 and Bundler, add the following to your Gemfile:

```ruby
group :test do
  gem "shoulda-kept-respond-with-content-type"
end

Shoulda will automatically include matchers into the appropriate example groups.