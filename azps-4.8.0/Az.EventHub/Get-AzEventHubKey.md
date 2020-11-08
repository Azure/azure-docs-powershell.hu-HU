---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184973"
---
# <span data-ttu-id="fc674-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="fc674-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="fc674-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc674-102">SYNOPSIS</span></span>
<span data-ttu-id="fc674-103">A megadott esemény-hubok engedélyezési szabályának elsődleges kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fc674-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="fc674-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc674-104">SYNTAX</span></span>

### <span data-ttu-id="fc674-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc674-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc674-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc674-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc674-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc674-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc674-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc674-108">DESCRIPTION</span></span>
<span data-ttu-id="fc674-109">A Get-AzEventHubKey parancsmag az elsődleges és a másodlagos connectionStrings, illetve a megadott névtér/esemény hubok/alias engedélyezési szabály részleteit adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fc674-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="fc674-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fc674-110">EXAMPLES</span></span>

### <span data-ttu-id="fc674-111">Példa 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="fc674-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="fc674-112">2. példa: EventHub</span><span class="sxs-lookup"><span data-stu-id="fc674-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="fc674-113">Az elsődleges és a másodlagos connectionStrings, valamint az engedélyezési szabály MyAuthRuleName tartozó kulcsok részleteit kapja meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="fc674-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="fc674-114">3. példa: alias (GeoRecovery-konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="fc674-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="fc674-115">Az elsődleges, a másodlagos, a AliasPrimary és a AliasSecondary connectionStrings és kulcsokat részletezi az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="fc674-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="fc674-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc674-116">PARAMETERS</span></span>

### <span data-ttu-id="fc674-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="fc674-117">-AliasName</span></span>
<span data-ttu-id="fc674-118">Alias neve</span><span class="sxs-lookup"><span data-stu-id="fc674-118">Alias Name</span></span>

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

### <span data-ttu-id="fc674-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc674-119">-DefaultProfile</span></span>
<span data-ttu-id="fc674-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc674-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc674-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fc674-121">-EventHub</span></span>
<span data-ttu-id="fc674-122">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="fc674-122">EventHub Name</span></span>

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

### <span data-ttu-id="fc674-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc674-123">-Name</span></span>
<span data-ttu-id="fc674-124">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="fc674-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="fc674-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc674-125">-Namespace</span></span>
<span data-ttu-id="fc674-126">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="fc674-126">Namespace Name</span></span>

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

### <span data-ttu-id="fc674-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc674-127">-ResourceGroupName</span></span>
<span data-ttu-id="fc674-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="fc674-128">Resource Group Name</span></span>

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

### <span data-ttu-id="fc674-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc674-129">CommonParameters</span></span>
<span data-ttu-id="fc674-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc674-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc674-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc674-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc674-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc674-132">INPUTS</span></span>

### <span data-ttu-id="fc674-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fc674-133">System.String</span></span>

## <span data-ttu-id="fc674-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc674-134">OUTPUTS</span></span>

### <span data-ttu-id="fc674-135">Microsoft. Azure. Command. EventHub. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="fc674-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="fc674-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc674-136">NOTES</span></span>

## <span data-ttu-id="fc674-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc674-137">RELATED LINKS</span></span>
