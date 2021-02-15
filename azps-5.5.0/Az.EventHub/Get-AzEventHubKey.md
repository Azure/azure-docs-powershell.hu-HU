---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147947"
---
# <span data-ttu-id="04cc1-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="04cc1-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="04cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="04cc1-103">Lekérte a megadott Eseményközpontok engedélyezési szabályának elsődleges kulcsának adatait.</span><span class="sxs-lookup"><span data-stu-id="04cc1-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="04cc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04cc1-104">SYNTAX</span></span>

### <span data-ttu-id="04cc1-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04cc1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04cc1-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="04cc1-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04cc1-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="04cc1-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04cc1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04cc1-108">DESCRIPTION</span></span>
<span data-ttu-id="04cc1-109">A Get-AzEventHubKey parancsmag a megadott NameSpace/Event Hubs/Alias engedélyezési szabály Elsődleges és Másodlagos kapcsolatok és kulcsok részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="04cc1-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="04cc1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04cc1-110">EXAMPLES</span></span>

### <span data-ttu-id="04cc1-111">1. példa: Namespace</span><span class="sxs-lookup"><span data-stu-id="04cc1-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="04cc1-112">2. példa: EventHub</span><span class="sxs-lookup"><span data-stu-id="04cc1-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="04cc1-113">A MyAuthRuleName engedélyezési szabály elsődleges és másodlagos kapcsolatainak adatait és \` kulcsait \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="04cc1-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="04cc1-114">3. példa: Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="04cc1-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="04cc1-115">A MyAuthRuleName engedélyezési szabály elsődleges, másodlagos, AliasPrimary és AliasSecondary kapcsolatok és kulcsok adatait \` \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="04cc1-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="04cc1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04cc1-116">PARAMETERS</span></span>

### <span data-ttu-id="04cc1-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="04cc1-117">-AliasName</span></span>
<span data-ttu-id="04cc1-118">Alias Name</span><span class="sxs-lookup"><span data-stu-id="04cc1-118">Alias Name</span></span>

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

### <span data-ttu-id="04cc1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04cc1-119">-DefaultProfile</span></span>
<span data-ttu-id="04cc1-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04cc1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04cc1-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="04cc1-121">-EventHub</span></span>
<span data-ttu-id="04cc1-122">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="04cc1-122">EventHub Name</span></span>

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

### <span data-ttu-id="04cc1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="04cc1-123">-Name</span></span>
<span data-ttu-id="04cc1-124">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="04cc1-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="04cc1-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="04cc1-125">-Namespace</span></span>
<span data-ttu-id="04cc1-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="04cc1-126">Namespace Name</span></span>

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

### <span data-ttu-id="04cc1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04cc1-127">-ResourceGroupName</span></span>
<span data-ttu-id="04cc1-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="04cc1-128">Resource Group Name</span></span>

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

### <span data-ttu-id="04cc1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04cc1-129">CommonParameters</span></span>
<span data-ttu-id="04cc1-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04cc1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04cc1-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04cc1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04cc1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04cc1-132">INPUTS</span></span>

### <span data-ttu-id="04cc1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="04cc1-133">System.String</span></span>

## <span data-ttu-id="04cc1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04cc1-134">OUTPUTS</span></span>

### <span data-ttu-id="04cc1-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="04cc1-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="04cc1-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04cc1-136">NOTES</span></span>

## <span data-ttu-id="04cc1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04cc1-137">RELATED LINKS</span></span>
