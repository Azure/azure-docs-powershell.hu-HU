---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: f9f4cc86a07c50718511c3ed0889d96f7acec9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938970"
---
# <span data-ttu-id="369e6-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="369e6-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="369e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="369e6-102">SYNOPSIS</span></span>
<span data-ttu-id="369e6-103">Szerezze be a CommunicationService szolgáltatást és tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="369e6-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="369e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="369e6-104">SYNTAX</span></span>

### <span data-ttu-id="369e6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="369e6-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="369e6-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="369e6-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="369e6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="369e6-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="369e6-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="369e6-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="369e6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="369e6-109">DESCRIPTION</span></span>
<span data-ttu-id="369e6-110">Szerezze be a CommunicationService szolgáltatást és tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="369e6-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="369e6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="369e6-111">EXAMPLES</span></span>

### <span data-ttu-id="369e6-112">1. példa: Előfizetés meglévő CommunicationServices szolgáltatásának felsorolása</span><span class="sxs-lookup"><span data-stu-id="369e6-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="369e6-113">Az adott előfizetésben található összes ACS-erőforrás listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="369e6-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="369e6-114">2. példa: Információk lekérte a megadott Azure Communication-erőforrást</span><span class="sxs-lookup"><span data-stu-id="369e6-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="369e6-115">Egy ACS-erőforrás adatait adja eredményül, ha talál egyező paramétert.</span><span class="sxs-lookup"><span data-stu-id="369e6-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="369e6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="369e6-116">PARAMETERS</span></span>

### <span data-ttu-id="369e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="369e6-117">-DefaultProfile</span></span>
<span data-ttu-id="369e6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="369e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="369e6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="369e6-119">-InputObject</span></span>
<span data-ttu-id="369e6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="369e6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="369e6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="369e6-121">-Name</span></span>
<span data-ttu-id="369e6-122">A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="369e6-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="369e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="369e6-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="369e6-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="369e6-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="369e6-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="369e6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="369e6-126">-SubscriptionId</span></span>
<span data-ttu-id="369e6-127">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="369e6-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="369e6-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="369e6-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="369e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369e6-129">CommonParameters</span></span>
<span data-ttu-id="369e6-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="369e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369e6-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="369e6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369e6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="369e6-132">INPUTS</span></span>

### <span data-ttu-id="369e6-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="369e6-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="369e6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="369e6-134">OUTPUTS</span></span>

### <span data-ttu-id="369e6-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="369e6-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="369e6-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="369e6-136">NOTES</span></span>

<span data-ttu-id="369e6-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="369e6-137">ALIASES</span></span>

<span data-ttu-id="369e6-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="369e6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="369e6-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="369e6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="369e6-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="369e6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="369e6-141">INPUTOBJECT: <ICommunicationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="369e6-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="369e6-142">`[CommunicationServiceName <String>]`: A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="369e6-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="369e6-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="369e6-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="369e6-144">`[Location <String>]`: Az Azure régió</span><span class="sxs-lookup"><span data-stu-id="369e6-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="369e6-145">`[OperationId <String>]`: Folyamatban lévő async-művelet azonosítója</span><span class="sxs-lookup"><span data-stu-id="369e6-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="369e6-146">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="369e6-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="369e6-147">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="369e6-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="369e6-148">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="369e6-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="369e6-149">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="369e6-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="369e6-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="369e6-150">RELATED LINKS</span></span>

