---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502591"
---
# <span data-ttu-id="a6505-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a6505-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="a6505-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6505-102">SYNOPSIS</span></span>
<span data-ttu-id="a6505-103">Egy engedélyezési szabály részleteit kapja meg, vagy megkapja az engedélyezési szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="a6505-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6505-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6505-104">SYNTAX</span></span>

### <span data-ttu-id="a6505-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6505-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6505-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6505-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6505-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6505-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6505-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6505-108">DESCRIPTION</span></span>
<span data-ttu-id="a6505-109">A Get-AzureRmEventHubAuthorizationRule parancsmag egy engedélyezési szabály részleteit vagy egy adott esemény központhoz tartozó összes engedélyezési szabály listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="a6505-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="a6505-110">Ha egy engedélyezési szabály neve meg van határozva, az adott egyetlen engedélyezési szabály részleteit adja vissza a függvény.</span><span class="sxs-lookup"><span data-stu-id="a6505-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="a6505-111">Ha egy engedélyezési szabály neve nem jelenik meg, akkor a megadott esemény központjának minden engedélyezési szabályát a program visszaadja.</span><span class="sxs-lookup"><span data-stu-id="a6505-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="a6505-112">Ha (katasztrófa-helyreállítási) alias név, a rendszer az aliashoz konfigurált névtér engedélyezési szabályának részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="a6505-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="a6505-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a6505-113">EXAMPLES</span></span>

### <span data-ttu-id="a6505-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a6505-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="a6505-115">Az \` MyAuthRuleName az \` esemény központi \` MyEventHubName kapja \` , amelyet a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="a6505-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="a6505-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="a6505-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="a6505-117">Beolvassa az összes engedélyezési szabály listáját az esemény központi \` MyEventHubName \` , amelyet a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="a6505-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="a6505-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="a6505-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="a6505-119">Az engedélyezési szabály \` MyAuthRuleName a \` névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="a6505-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="a6505-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6505-120">PARAMETERS</span></span>

### <span data-ttu-id="a6505-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a6505-121">-AliasName</span></span>
<span data-ttu-id="a6505-122">Alias neve</span><span class="sxs-lookup"><span data-stu-id="a6505-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6505-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6505-123">-DefaultProfile</span></span>
<span data-ttu-id="a6505-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6505-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6505-125">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="a6505-125">-Eventhub</span></span>
<span data-ttu-id="a6505-126">Eventhub neve</span><span class="sxs-lookup"><span data-stu-id="a6505-126">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6505-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6505-127">-Name</span></span>
<span data-ttu-id="a6505-128">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="a6505-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6505-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a6505-129">-Namespace</span></span>
<span data-ttu-id="a6505-130">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a6505-130">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6505-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6505-131">-ResourceGroupName</span></span>
<span data-ttu-id="a6505-132">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a6505-132">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6505-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6505-133">CommonParameters</span></span>
<span data-ttu-id="a6505-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6505-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a6505-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6505-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6505-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6505-136">INPUTS</span></span>

### <span data-ttu-id="a6505-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a6505-137">System.String</span></span>


## <span data-ttu-id="a6505-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6505-138">OUTPUTS</span></span>

### <span data-ttu-id="a6505-139">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. EventHub, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a6505-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="a6505-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6505-140">NOTES</span></span>

## <span data-ttu-id="a6505-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6505-141">RELATED LINKS</span></span>
