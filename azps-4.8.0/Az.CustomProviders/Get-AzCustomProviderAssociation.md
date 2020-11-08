---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185063"
---
# <span data-ttu-id="13b7c-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="13b7c-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="13b7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="13b7c-103">Társítás kérése</span><span class="sxs-lookup"><span data-stu-id="13b7c-103">Get an association.</span></span>

## <span data-ttu-id="13b7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13b7c-104">SYNTAX</span></span>

### <span data-ttu-id="13b7c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13b7c-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="13b7c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="13b7c-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="13b7c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="13b7c-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="13b7c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="13b7c-108">DESCRIPTION</span></span>
<span data-ttu-id="13b7c-109">Társítás kérése</span><span class="sxs-lookup"><span data-stu-id="13b7c-109">Get an association.</span></span>

## <span data-ttu-id="13b7c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="13b7c-110">EXAMPLES</span></span>

### <span data-ttu-id="13b7c-111">1. példa: egyéni szolgáltatói társítások listázása</span><span class="sxs-lookup"><span data-stu-id="13b7c-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="13b7c-112">Felsorolja az összes egyéni szolgáltató társítását egy adott hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="13b7c-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="13b7c-113">2. példa: társítás beszerzése</span><span class="sxs-lookup"><span data-stu-id="13b7c-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="13b7c-114">Egyetlen CustomProvider-társítás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="13b7c-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="13b7c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13b7c-115">PARAMETERS</span></span>

### <span data-ttu-id="13b7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b7c-116">-DefaultProfile</span></span>
<span data-ttu-id="13b7c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13b7c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b7c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13b7c-118">-InputObject</span></span>
<span data-ttu-id="13b7c-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="13b7c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="13b7c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13b7c-120">-Name</span></span>
<span data-ttu-id="13b7c-121">A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="13b7c-121">The name of the association.</span></span>

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

### <span data-ttu-id="13b7c-122">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="13b7c-122">-Scope</span></span>
<span data-ttu-id="13b7c-123">A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="13b7c-123">The scope of the association.</span></span>

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

### <span data-ttu-id="13b7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b7c-124">CommonParameters</span></span>
<span data-ttu-id="13b7c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13b7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b7c-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="13b7c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b7c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b7c-127">INPUTS</span></span>

### <span data-ttu-id="13b7c-128">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="13b7c-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="13b7c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b7c-129">OUTPUTS</span></span>

### <span data-ttu-id="13b7c-130">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. modellek. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="13b7c-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="13b7c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13b7c-131">NOTES</span></span>

<span data-ttu-id="13b7c-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="13b7c-132">ALIASES</span></span>

<span data-ttu-id="13b7c-133">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="13b7c-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13b7c-134">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="13b7c-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13b7c-135">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="13b7c-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13b7c-136">INPUTOBJECT <ICustomProvidersIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="13b7c-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13b7c-137">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="13b7c-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="13b7c-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="13b7c-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13b7c-139">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13b7c-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="13b7c-140">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="13b7c-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="13b7c-141">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="13b7c-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="13b7c-142">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13b7c-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="13b7c-143">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="13b7c-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="13b7c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13b7c-144">RELATED LINKS</span></span>

