---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: ec52bea37eed3bb785da80beb8dfba02d0a426cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143835"
---
# <span data-ttu-id="be0ac-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="be0ac-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="be0ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="be0ac-103">A Tartományszolgáltatás lekérése művelet lekéri a tartományszolgáltatás json-ábrázolását.</span><span class="sxs-lookup"><span data-stu-id="be0ac-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="be0ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="be0ac-104">SYNTAX</span></span>

### <span data-ttu-id="be0ac-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be0ac-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="be0ac-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="be0ac-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="be0ac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="be0ac-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="be0ac-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="be0ac-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="be0ac-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="be0ac-109">DESCRIPTION</span></span>
<span data-ttu-id="be0ac-110">A Tartományszolgáltatás lekérése művelet lekéri a tartományszolgáltatás json-ábrázolását.</span><span class="sxs-lookup"><span data-stu-id="be0ac-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="be0ac-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="be0ac-111">EXAMPLES</span></span>

### <span data-ttu-id="be0ac-112">1. példa: Az összes ADDomainService be szerezni alapértelmezés szerint</span><span class="sxs-lookup"><span data-stu-id="be0ac-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="be0ac-113">Az összes ADDomainService be szerezni alapértelmezés szerint</span><span class="sxs-lookup"><span data-stu-id="be0ac-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="be0ac-114">2. példa: Az ADDomainService By ResourceGroup és neve</span><span class="sxs-lookup"><span data-stu-id="be0ac-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="be0ac-115">Get ADDomainService By ResourceGroup and name</span><span class="sxs-lookup"><span data-stu-id="be0ac-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="be0ac-116">3. példa: Az ADDomainService by ResourceGroup összes szolgáltatásának be szereznie</span><span class="sxs-lookup"><span data-stu-id="be0ac-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="be0ac-117">Az összes ADDomainService by ResourceGroup lekért szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="be0ac-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="be0ac-118">4. példa: Az ADDomainService lekérte az InputObject eszközét</span><span class="sxs-lookup"><span data-stu-id="be0ac-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="be0ac-119">Az ADDomainService lekérte az InputObject eszközét</span><span class="sxs-lookup"><span data-stu-id="be0ac-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="be0ac-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be0ac-120">PARAMETERS</span></span>

### <span data-ttu-id="be0ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0ac-121">-DefaultProfile</span></span>
<span data-ttu-id="be0ac-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be0ac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be0ac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be0ac-123">-InputObject</span></span>
<span data-ttu-id="be0ac-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="be0ac-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be0ac-125">-Name</span><span class="sxs-lookup"><span data-stu-id="be0ac-125">-Name</span></span>
<span data-ttu-id="be0ac-126">A tartományszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="be0ac-126">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be0ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be0ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="be0ac-128">A felhasználó előfizetésében található erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="be0ac-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="be0ac-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="be0ac-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="be0ac-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be0ac-130">-SubscriptionId</span></span>
<span data-ttu-id="be0ac-131">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="be0ac-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="be0ac-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="be0ac-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="be0ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0ac-133">CommonParameters</span></span>
<span data-ttu-id="be0ac-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be0ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0ac-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be0ac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0ac-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be0ac-136">INPUTS</span></span>

### <span data-ttu-id="be0ac-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="be0ac-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="be0ac-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be0ac-138">OUTPUTS</span></span>

### <span data-ttu-id="be0ac-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="be0ac-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="be0ac-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="be0ac-140">NOTES</span></span>

<span data-ttu-id="be0ac-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="be0ac-141">ALIASES</span></span>

<span data-ttu-id="be0ac-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="be0ac-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be0ac-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="be0ac-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be0ac-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be0ac-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be0ac-145">INPUTOBJECT: <IAdDomainServicesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="be0ac-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be0ac-146">`[DomainServiceName <String>]`: A tartományszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="be0ac-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="be0ac-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="be0ac-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be0ac-148">`[ResourceGroupName <String>]`: A felhasználó előfizetésében található erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="be0ac-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="be0ac-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="be0ac-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="be0ac-150">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="be0ac-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="be0ac-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="be0ac-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="be0ac-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be0ac-152">RELATED LINKS</span></span>

