---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505031"
---
# <span data-ttu-id="6181c-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="6181c-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="6181c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6181c-102">SYNOPSIS</span></span>
<span data-ttu-id="6181c-103">A megadott esemény-hubok engedélyezési szabályának elsődleges kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6181c-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6181c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6181c-104">SYNTAX</span></span>

### <span data-ttu-id="6181c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6181c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="6181c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6181c-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="6181c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6181c-107">DESCRIPTION</span></span>
<span data-ttu-id="6181c-108">A Get-AzureRmEventHubKey parancsmag az elsődleges és a másodlagos connectionStrings, valamint a megadott esemény-hubok engedélyezési szabályának adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6181c-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="6181c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6181c-109">EXAMPLES</span></span>

### <span data-ttu-id="6181c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6181c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="6181c-111">Az elsődleges és a másodlagos connectionStrings, valamint az engedélyezési szabály MyAuthRuleName tartozó kulcsok részleteit kapja meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="6181c-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="6181c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6181c-112">PARAMETERS</span></span>

### <span data-ttu-id="6181c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6181c-113">-ResourceGroupName</span></span>
<span data-ttu-id="6181c-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6181c-114">Resource group name.</span></span>

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

### <span data-ttu-id="6181c-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6181c-115">-EventHub</span></span>
<span data-ttu-id="6181c-116">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="6181c-116">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6181c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6181c-117">-Name</span></span>
<span data-ttu-id="6181c-118">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="6181c-118">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6181c-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6181c-119">-Namespace</span></span>
<span data-ttu-id="6181c-120">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="6181c-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6181c-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6181c-121">INPUTS</span></span>

### <span data-ttu-id="6181c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6181c-122">System.String</span></span>

## <span data-ttu-id="6181c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6181c-123">OUTPUTS</span></span>

### <span data-ttu-id="6181c-124">Microsoft. Azure. Command. EventHub. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6181c-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="6181c-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6181c-125">NOTES</span></span>

## <span data-ttu-id="6181c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6181c-126">RELATED LINKS</span></span>

