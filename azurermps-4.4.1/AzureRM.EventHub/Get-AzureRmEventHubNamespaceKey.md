---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505020"
---
# <span data-ttu-id="cc3b7-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="cc3b7-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="cc3b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3b7-103">A megadott esemény-hubok névtér-engedélyezési szabályának engedélyezési szabályához tartozó elsődleges, másodlagos connectionStrings és kulcsok részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cc3b7-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc3b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc3b7-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="cc3b7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc3b7-105">DESCRIPTION</span></span>
<span data-ttu-id="cc3b7-106">A Get-AzureRmEventHubNamespaceKey parancsmag a megadott engedélyezési szabály elsődleges és másodlagos connectionStrings és kulcsait adja meg a megadott esemény-hubok névtérben.</span><span class="sxs-lookup"><span data-stu-id="cc3b7-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="cc3b7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cc3b7-107">EXAMPLES</span></span>

### <span data-ttu-id="cc3b7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc3b7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="cc3b7-109">Az connectionStrings- \` MyAuthRuleName az \` esemény-hubok névtér \` -MyNamespaceName az \` \` első, \` a másodlagos és a kulcsok kiértékeléséhez szükséges adatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="cc3b7-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="cc3b7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc3b7-110">PARAMETERS</span></span>

### <span data-ttu-id="cc3b7-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="cc3b7-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="cc3b7-112">Az engedélyezési szabály neve az esemény-hubok névtérben.</span><span class="sxs-lookup"><span data-stu-id="cc3b7-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc3b7-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="cc3b7-113">-NamespaceName</span></span>
<span data-ttu-id="cc3b7-114">Az esemény hubok névterének neve.</span><span class="sxs-lookup"><span data-stu-id="cc3b7-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc3b7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc3b7-115">-ResourceGroupName</span></span>
<span data-ttu-id="cc3b7-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="cc3b7-116">Resource group name.</span></span>

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

## <span data-ttu-id="cc3b7-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc3b7-117">INPUTS</span></span>

### <span data-ttu-id="cc3b7-118">System. String</span><span class="sxs-lookup"><span data-stu-id="cc3b7-118">System.String</span></span>

## <span data-ttu-id="cc3b7-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc3b7-119">OUTPUTS</span></span>

### <span data-ttu-id="cc3b7-120">Microsoft. Azure. Command. EventHub. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="cc3b7-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="cc3b7-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc3b7-121">NOTES</span></span>

## <span data-ttu-id="cc3b7-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc3b7-122">RELATED LINKS</span></span>

