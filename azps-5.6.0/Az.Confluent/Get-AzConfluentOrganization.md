---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012597"
---
# <span data-ttu-id="5c315-101">Get-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="5c315-101">Get-AzConfluentOrganization</span></span>

## <span data-ttu-id="5c315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c315-102">SYNOPSIS</span></span>
<span data-ttu-id="5c315-103">Egy adott szervezeti erőforrás tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="5c315-103">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="5c315-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5c315-104">SYNTAX</span></span>

### <span data-ttu-id="5c315-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c315-105">List (Default)</span></span>
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5c315-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="5c315-106">Get</span></span>
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5c315-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5c315-107">GetViaIdentity</span></span>
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c315-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="5c315-108">List1</span></span>
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5c315-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5c315-109">DESCRIPTION</span></span>
<span data-ttu-id="5c315-110">Egy adott szervezeti erőforrás tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="5c315-110">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="5c315-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5c315-111">EXAMPLES</span></span>

### <span data-ttu-id="5c315-112">1. példa: Az előfizetések alatt található összes összefolyásos szervezet felsorolása</span><span class="sxs-lookup"><span data-stu-id="5c315-112">Example 1: List all confluent organizations under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

<span data-ttu-id="5c315-113">Ez a parancs felsorolja az előfizetés alatt található összes összefolyásos szervezetet.</span><span class="sxs-lookup"><span data-stu-id="5c315-113">This command lists all confluent organizations under a subscription.</span></span>

### <span data-ttu-id="5c315-114">2. példa: Egy erőforráscsoport összes összefolyásos szervezetének felsorolása</span><span class="sxs-lookup"><span data-stu-id="5c315-114">Example 2: List all confluent organizations under a resource group</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

<span data-ttu-id="5c315-115">Ez a parancs felsorolja egy erőforráscsoport összes összefolyásos szervezetét.</span><span class="sxs-lookup"><span data-stu-id="5c315-115">This command lists all confluent organizations under a resource group.</span></span>

### <span data-ttu-id="5c315-116">3. példa: Összefolyásos szervezet elnevezése</span><span class="sxs-lookup"><span data-stu-id="5c315-116">Example 3: Get a confluent organization by name</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

<span data-ttu-id="5c315-117">Ez a parancs egy összefolyásos szervezetet kap név szerint.</span><span class="sxs-lookup"><span data-stu-id="5c315-117">This command gets a confluent organization by name.</span></span>

### <span data-ttu-id="5c315-118">4. példa: Összefolyásos szervezet létrehozása folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="5c315-118">Example 4: Get a confluent organization by pipeline</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="5c315-119">Ez a parancs folyamat szerint összefolyásos szervezetet kap.</span><span class="sxs-lookup"><span data-stu-id="5c315-119">This command gets a confluent organization by pipeline.</span></span>

## <span data-ttu-id="5c315-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c315-120">PARAMETERS</span></span>

### <span data-ttu-id="5c315-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c315-121">-DefaultProfile</span></span>
<span data-ttu-id="5c315-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c315-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c315-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c315-123">-InputObject</span></span>
<span data-ttu-id="5c315-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5c315-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c315-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5c315-125">-Name</span></span>
<span data-ttu-id="5c315-126">Szervezet erőforrásneve</span><span class="sxs-lookup"><span data-stu-id="5c315-126">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c315-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c315-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c315-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5c315-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c315-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c315-129">-SubscriptionId</span></span>
<span data-ttu-id="5c315-130">Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="5c315-130">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c315-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c315-131">CommonParameters</span></span>
<span data-ttu-id="5c315-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c315-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c315-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c315-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c315-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c315-134">INPUTS</span></span>

### <span data-ttu-id="5c315-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="5c315-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="5c315-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c315-136">OUTPUTS</span></span>

### <span data-ttu-id="5c315-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="5c315-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="5c315-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5c315-138">NOTES</span></span>

<span data-ttu-id="5c315-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5c315-139">ALIASES</span></span>

<span data-ttu-id="5c315-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5c315-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5c315-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5c315-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c315-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5c315-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5c315-143">INPUTOBJECT: <IConfluentIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5c315-143">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c315-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5c315-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c315-145">`[OrganizationName <String>]`: Szervezet erőforrásneve</span><span class="sxs-lookup"><span data-stu-id="5c315-145">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="5c315-146">`[ResourceGroupName <String>]`: Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5c315-146">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="5c315-147">`[SubscriptionId <String>]`: Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="5c315-147">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="5c315-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c315-148">RELATED LINKS</span></span>

