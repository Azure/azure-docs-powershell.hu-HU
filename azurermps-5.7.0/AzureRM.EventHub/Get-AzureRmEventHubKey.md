---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: f8a9f074398df5ce9d8464adf3c22a65d14784b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502583"
---
# <span data-ttu-id="a9d39-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="a9d39-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="a9d39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9d39-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d39-103">A megadott esemény-hubok engedélyezési szabályának elsődleges kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a9d39-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9d39-104">SYNTAX</span></span>

### <span data-ttu-id="a9d39-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9d39-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d39-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9d39-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d39-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9d39-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9d39-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9d39-108">DESCRIPTION</span></span>
<span data-ttu-id="a9d39-109">A Get-AzureRmEventHubKey parancsmag az elsődleges és a másodlagos connectionStrings, illetve a megadott névtér/esemény hubok/alias engedélyezési szabály részleteit adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a9d39-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="a9d39-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a9d39-110">EXAMPLES</span></span>

### <span data-ttu-id="a9d39-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a9d39-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="a9d39-112">Az elsődleges és a másodlagos connectionStrings, valamint az engedélyezési szabály MyAuthRuleName tartozó kulcsok részleteit kapja meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="a9d39-112">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="a9d39-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a9d39-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="a9d39-114">Az elsődleges, a másodlagos, a AliasPrimary és a AliasSecondary connectionStrings és kulcsokat részletezi az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="a9d39-114">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="a9d39-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9d39-115">PARAMETERS</span></span>

### <span data-ttu-id="a9d39-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a9d39-116">-AliasName</span></span>
<span data-ttu-id="a9d39-117">Alias neve</span><span class="sxs-lookup"><span data-stu-id="a9d39-117">Alias Name</span></span>

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

### <span data-ttu-id="a9d39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d39-118">-DefaultProfile</span></span>
<span data-ttu-id="a9d39-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9d39-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9d39-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a9d39-120">-EventHub</span></span>
<span data-ttu-id="a9d39-121">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="a9d39-121">EventHub Name</span></span>

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

### <span data-ttu-id="a9d39-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9d39-122">-Name</span></span>
<span data-ttu-id="a9d39-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="a9d39-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d39-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a9d39-124">-Namespace</span></span>
<span data-ttu-id="a9d39-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a9d39-125">Namespace Name</span></span>

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

### <span data-ttu-id="a9d39-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d39-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9d39-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a9d39-127">Resource Group Name</span></span>

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

### <span data-ttu-id="a9d39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d39-128">CommonParameters</span></span>
<span data-ttu-id="a9d39-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9d39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a9d39-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d39-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d39-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9d39-131">INPUTS</span></span>

### <span data-ttu-id="a9d39-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a9d39-132">System.String</span></span>


## <span data-ttu-id="a9d39-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9d39-133">OUTPUTS</span></span>

### <span data-ttu-id="a9d39-134">Microsoft. Azure. Command. EventHub. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a9d39-134">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="a9d39-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9d39-135">NOTES</span></span>

## <span data-ttu-id="a9d39-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9d39-136">RELATED LINKS</span></span>
