---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 27be06fb85cc4bd1dc38dd7a123205d3ba7ff4d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842349"
---
# <span data-ttu-id="b21f2-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="b21f2-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="b21f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b21f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b21f2-103">A megadott esemény-hubok engedélyezési szabályának elsődleges kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b21f2-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b21f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b21f2-104">SYNTAX</span></span>

### <span data-ttu-id="b21f2-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b21f2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b21f2-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b21f2-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b21f2-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="b21f2-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b21f2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b21f2-108">DESCRIPTION</span></span>
<span data-ttu-id="b21f2-109">A Get-AzEventHubKey parancsmag az elsődleges és a másodlagos connectionStrings, illetve a megadott névtér/esemény hubok/alias engedélyezési szabály részleteit adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b21f2-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="b21f2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b21f2-110">EXAMPLES</span></span>

### <span data-ttu-id="b21f2-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="b21f2-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="b21f2-112">Példa 2-EventHub</span><span class="sxs-lookup"><span data-stu-id="b21f2-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="b21f2-113">Az elsődleges és a másodlagos connectionStrings, valamint az engedélyezési szabály MyAuthRuleName tartozó kulcsok részleteit kapja meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="b21f2-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="b21f2-114">Példa 3 – alias (GeoRecovery-konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="b21f2-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="b21f2-115">Az elsődleges, a másodlagos, a AliasPrimary és a AliasSecondary connectionStrings és kulcsokat részletezi az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="b21f2-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="b21f2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b21f2-116">PARAMETERS</span></span>

### <span data-ttu-id="b21f2-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="b21f2-117">-AliasName</span></span>
<span data-ttu-id="b21f2-118">Alias neve</span><span class="sxs-lookup"><span data-stu-id="b21f2-118">Alias Name</span></span>

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

### <span data-ttu-id="b21f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21f2-119">-DefaultProfile</span></span>
<span data-ttu-id="b21f2-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b21f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b21f2-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b21f2-121">-EventHub</span></span>
<span data-ttu-id="b21f2-122">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="b21f2-122">EventHub Name</span></span>

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

### <span data-ttu-id="b21f2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b21f2-123">-Name</span></span>
<span data-ttu-id="b21f2-124">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="b21f2-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b21f2-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b21f2-125">-Namespace</span></span>
<span data-ttu-id="b21f2-126">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b21f2-126">Namespace Name</span></span>

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

### <span data-ttu-id="b21f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b21f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="b21f2-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b21f2-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b21f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21f2-129">CommonParameters</span></span>
<span data-ttu-id="b21f2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b21f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21f2-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b21f2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21f2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b21f2-132">INPUTS</span></span>

### <span data-ttu-id="b21f2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b21f2-133">System.String</span></span>

## <span data-ttu-id="b21f2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b21f2-134">OUTPUTS</span></span>

### <span data-ttu-id="b21f2-135">Microsoft. Azure. Command. EventHub. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b21f2-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="b21f2-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b21f2-136">NOTES</span></span>

## <span data-ttu-id="b21f2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b21f2-137">RELATED LINKS</span></span>
