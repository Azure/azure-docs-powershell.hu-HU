---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163899"
---
# <span data-ttu-id="52df9-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="52df9-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="52df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52df9-102">SYNOPSIS</span></span>
<span data-ttu-id="52df9-103">Társítás lekérte.</span><span class="sxs-lookup"><span data-stu-id="52df9-103">Get an association.</span></span>

## <span data-ttu-id="52df9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="52df9-104">SYNTAX</span></span>

### <span data-ttu-id="52df9-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52df9-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="52df9-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="52df9-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="52df9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52df9-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="52df9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="52df9-108">DESCRIPTION</span></span>
<span data-ttu-id="52df9-109">Társítás lekérte.</span><span class="sxs-lookup"><span data-stu-id="52df9-109">Get an association.</span></span>

## <span data-ttu-id="52df9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="52df9-110">EXAMPLES</span></span>

### <span data-ttu-id="52df9-111">1. példa: Egyéni szolgáltató-társítások felsorolása</span><span class="sxs-lookup"><span data-stu-id="52df9-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="52df9-112">List all custom provider associations for a given scope.</span><span class="sxs-lookup"><span data-stu-id="52df9-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="52df9-113">2. példa: Társítás lekérte</span><span class="sxs-lookup"><span data-stu-id="52df9-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="52df9-114">Részletek lekérte egyetlen CustomProvider-társítás adatait</span><span class="sxs-lookup"><span data-stu-id="52df9-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="52df9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52df9-115">PARAMETERS</span></span>

### <span data-ttu-id="52df9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52df9-116">-DefaultProfile</span></span>
<span data-ttu-id="52df9-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52df9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52df9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52df9-118">-InputObject</span></span>
<span data-ttu-id="52df9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="52df9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52df9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="52df9-120">-Name</span></span>
<span data-ttu-id="52df9-121">A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="52df9-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52df9-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="52df9-122">-Scope</span></span>
<span data-ttu-id="52df9-123">A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="52df9-123">The scope of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52df9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52df9-124">CommonParameters</span></span>
<span data-ttu-id="52df9-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52df9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52df9-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52df9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52df9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52df9-127">INPUTS</span></span>

### <span data-ttu-id="52df9-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="52df9-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="52df9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52df9-129">OUTPUTS</span></span>

### <span data-ttu-id="52df9-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="52df9-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="52df9-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="52df9-131">NOTES</span></span>

<span data-ttu-id="52df9-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="52df9-132">ALIASES</span></span>

<span data-ttu-id="52df9-133">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="52df9-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52df9-134">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="52df9-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52df9-135">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52df9-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52df9-136">INPUTOBJECT: <ICustomProvidersIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="52df9-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52df9-137">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="52df9-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="52df9-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="52df9-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52df9-139">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52df9-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="52df9-140">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="52df9-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="52df9-141">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="52df9-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="52df9-142">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="52df9-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="52df9-143">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-00000-0000000000000)</span><span class="sxs-lookup"><span data-stu-id="52df9-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="52df9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52df9-144">RELATED LINKS</span></span>

