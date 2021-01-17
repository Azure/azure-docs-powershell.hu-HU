---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323563"
---
# <span data-ttu-id="3bb6b-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="3bb6b-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="3bb6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bb6b-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb6b-103">Lekérte a megadott Eseményközpontok engedélyezési szabályának elsődleges kulcsának adatait.</span><span class="sxs-lookup"><span data-stu-id="3bb6b-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="3bb6b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3bb6b-104">SYNTAX</span></span>

### <span data-ttu-id="3bb6b-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bb6b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bb6b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3bb6b-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bb6b-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="3bb6b-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bb6b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3bb6b-108">DESCRIPTION</span></span>
<span data-ttu-id="3bb6b-109">A Get-AzEventHubKey parancsmag a megadott NameSpace/Event Hubs/Alias engedélyezési szabály Elsődleges és Másodlagos kapcsolatok és kulcsok részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="3bb6b-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="3bb6b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3bb6b-110">EXAMPLES</span></span>

### <span data-ttu-id="3bb6b-111">1. példa: Namespace</span><span class="sxs-lookup"><span data-stu-id="3bb6b-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="3bb6b-112">2. példa: EventHub</span><span class="sxs-lookup"><span data-stu-id="3bb6b-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="3bb6b-113">A MyAuthRuleName engedélyezési szabály elsődleges és másodlagos kapcsolatainak adatait és \` kulcsait \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3bb6b-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="3bb6b-114">3. példa: Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="3bb6b-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="3bb6b-115">A MyAuthRuleName engedélyezési szabály elsődleges, másodlagos, AliasPrimary és AliasSecondary kapcsolatok és kulcsok adatait \` \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3bb6b-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="3bb6b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bb6b-116">PARAMETERS</span></span>

### <span data-ttu-id="3bb6b-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="3bb6b-117">-AliasName</span></span>
<span data-ttu-id="3bb6b-118">Alias Name</span><span class="sxs-lookup"><span data-stu-id="3bb6b-118">Alias Name</span></span>

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

### <span data-ttu-id="3bb6b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb6b-119">-DefaultProfile</span></span>
<span data-ttu-id="3bb6b-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bb6b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb6b-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3bb6b-121">-EventHub</span></span>
<span data-ttu-id="3bb6b-122">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="3bb6b-122">EventHub Name</span></span>

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

### <span data-ttu-id="3bb6b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3bb6b-123">-Name</span></span>
<span data-ttu-id="3bb6b-124">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="3bb6b-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="3bb6b-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3bb6b-125">-Namespace</span></span>
<span data-ttu-id="3bb6b-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3bb6b-126">Namespace Name</span></span>

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

### <span data-ttu-id="3bb6b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb6b-127">-ResourceGroupName</span></span>
<span data-ttu-id="3bb6b-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3bb6b-128">Resource Group Name</span></span>

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

### <span data-ttu-id="3bb6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb6b-129">CommonParameters</span></span>
<span data-ttu-id="3bb6b-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb6b-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb6b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb6b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bb6b-132">INPUTS</span></span>

### <span data-ttu-id="3bb6b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3bb6b-133">System.String</span></span>

## <span data-ttu-id="3bb6b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bb6b-134">OUTPUTS</span></span>

### <span data-ttu-id="3bb6b-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="3bb6b-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="3bb6b-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3bb6b-136">NOTES</span></span>

## <span data-ttu-id="3bb6b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bb6b-137">RELATED LINKS</span></span>
