---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: c22bb41702bb4e338d0548be6c7544d597ef0230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500223"
---
# <span data-ttu-id="48e61-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="48e61-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="48e61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48e61-102">SYNOPSIS</span></span>
<span data-ttu-id="48e61-103">A megadott esemény-hubok engedélyezési szabályának elsődleges kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="48e61-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48e61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48e61-104">SYNTAX</span></span>

### <span data-ttu-id="48e61-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48e61-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48e61-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="48e61-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48e61-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="48e61-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48e61-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="48e61-108">DESCRIPTION</span></span>
<span data-ttu-id="48e61-109">A Get-AzureRmEventHubKey parancsmag az elsődleges és a másodlagos connectionStrings, illetve a megadott névtér/esemény hubok/alias engedélyezési szabály részleteit adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="48e61-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="48e61-110">Példák</span><span class="sxs-lookup"><span data-stu-id="48e61-110">EXAMPLES</span></span>

### <span data-ttu-id="48e61-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="48e61-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="48e61-112">Példa 2-EventHub</span><span class="sxs-lookup"><span data-stu-id="48e61-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="48e61-113">Az elsődleges és a másodlagos connectionStrings, valamint az engedélyezési szabály MyAuthRuleName tartozó kulcsok részleteit kapja meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="48e61-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="48e61-114">Példa 3 – alias (GeoRecovery-konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="48e61-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="48e61-115">Az elsődleges, a másodlagos, a AliasPrimary és a AliasSecondary connectionStrings és kulcsokat részletezi az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="48e61-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="48e61-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48e61-116">PARAMETERS</span></span>

### <span data-ttu-id="48e61-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="48e61-117">-AliasName</span></span>
<span data-ttu-id="48e61-118">Alias neve</span><span class="sxs-lookup"><span data-stu-id="48e61-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e61-119">-DefaultProfile</span></span>
<span data-ttu-id="48e61-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48e61-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e61-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="48e61-121">-EventHub</span></span>
<span data-ttu-id="48e61-122">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="48e61-122">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e61-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48e61-123">-Name</span></span>
<span data-ttu-id="48e61-124">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="48e61-124">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e61-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="48e61-125">-Namespace</span></span>
<span data-ttu-id="48e61-126">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="48e61-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e61-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e61-127">-ResourceGroupName</span></span>
<span data-ttu-id="48e61-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="48e61-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e61-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e61-129">CommonParameters</span></span>
<span data-ttu-id="48e61-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48e61-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e61-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e61-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e61-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48e61-132">INPUTS</span></span>

### <span data-ttu-id="48e61-133">System. String</span><span class="sxs-lookup"><span data-stu-id="48e61-133">System.String</span></span>

## <span data-ttu-id="48e61-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48e61-134">OUTPUTS</span></span>

### <span data-ttu-id="48e61-135">Microsoft. Azure. Command. EventHub. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="48e61-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="48e61-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48e61-136">NOTES</span></span>

## <span data-ttu-id="48e61-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48e61-137">RELATED LINKS</span></span>
