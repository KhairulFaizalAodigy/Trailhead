<aura:component>
    <aura:attribute name="messages" type="List"
        default="['You look nice today.',
            'Great weather we\'re having.',
            'How are you?']"/>

    <h1>Hello Playground</h1>
    <p>Silly fun with attributes and expressions.</p>

    <h2>List Items</h2>
    <p><c:helloMessage message="{!v.messages[0]}"/></p>
    <p><c:helloMessage message="{!v.messages[1]}"/></p>
    <p><c:helloMessage message="{!v.messages[2]}"/></p>

    <h2>List Iteration</h2>
    <aura:iteration items="{!v.messages}" var="msg">
        <p><c:helloMessage message="{!msg}"/></p>
    </aura:iteration>

    <h2>Conditional Expressions and Global Value Providers</h2>
    <aura:if isTrue="{!$Browser.isIPhone}">
        <p><c:helloMessage message="{!v.messages[0]}"/></p>
    <aura:set attribute="else">
        <p><c:helloMessage message="{!v.messages[1]}"/></p>
        </aura:set>
    </aura:if>
</aura:component>
