---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369177"
---
# <span data-ttu-id="cee6b-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="cee6b-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="cee6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cee6b-102">SYNOPSIS</span></span>
<span data-ttu-id="cee6b-103">Társítás lekérte.</span><span class="sxs-lookup"><span data-stu-id="cee6b-103">Get an association.</span></span>

## <span data-ttu-id="cee6b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cee6b-104">SYNTAX</span></span>

### <span data-ttu-id="cee6b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cee6b-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cee6b-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="cee6b-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cee6b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cee6b-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cee6b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cee6b-108">DESCRIPTION</span></span>
<span data-ttu-id="cee6b-109">Társítás lekérte.</span><span class="sxs-lookup"><span data-stu-id="cee6b-109">Get an association.</span></span>

## <span data-ttu-id="cee6b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cee6b-110">EXAMPLES</span></span>

### <span data-ttu-id="cee6b-111">1. példa: Egyéni szolgáltató-társítások felsorolása</span><span class="sxs-lookup"><span data-stu-id="cee6b-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="cee6b-112">List all custom provider associations for a given scope.</span><span class="sxs-lookup"><span data-stu-id="cee6b-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="cee6b-113">2. példa: Társítás lekérte</span><span class="sxs-lookup"><span data-stu-id="cee6b-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="cee6b-114">Részletek lekérte egyetlen CustomProvider-társítás adatait</span><span class="sxs-lookup"><span data-stu-id="cee6b-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="cee6b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cee6b-115">PARAMETERS</span></span>

### <span data-ttu-id="cee6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee6b-116">-DefaultProfile</span></span>
<span data-ttu-id="cee6b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cee6b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cee6b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cee6b-118">-InputObject</span></span>
<span data-ttu-id="cee6b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cee6b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cee6b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cee6b-120">-Name</span></span>
<span data-ttu-id="cee6b-121">A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="cee6b-121">The name of the association.</span></span>

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

### <span data-ttu-id="cee6b-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="cee6b-122">-Scope</span></span>
<span data-ttu-id="cee6b-123">A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="cee6b-123">The scope of the association.</span></span>

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

### <span data-ttu-id="cee6b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee6b-124">CommonParameters</span></span>
<span data-ttu-id="cee6b-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee6b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee6b-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cee6b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee6b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cee6b-127">INPUTS</span></span>

### <span data-ttu-id="cee6b-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="cee6b-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="cee6b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cee6b-129">OUTPUTS</span></span>

### <span data-ttu-id="cee6b-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="cee6b-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="cee6b-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cee6b-131">NOTES</span></span>

<span data-ttu-id="cee6b-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cee6b-132">ALIASES</span></span>

<span data-ttu-id="cee6b-133">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="cee6b-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cee6b-134">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="cee6b-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cee6b-135">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cee6b-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cee6b-136">INPUTOBJECT: <ICustomProvidersIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="cee6b-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cee6b-137">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="cee6b-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="cee6b-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="cee6b-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cee6b-139">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cee6b-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cee6b-140">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="cee6b-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="cee6b-141">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="cee6b-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="cee6b-142">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cee6b-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="cee6b-143">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="cee6b-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="cee6b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cee6b-144">RELATED LINKS</span></span>

