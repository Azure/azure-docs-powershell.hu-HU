---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205006"
---
# <span data-ttu-id="bf8c6-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="bf8c6-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="bf8c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8c6-103">Művelet egy meglévő CommunicationService frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="bf8c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bf8c6-104">SYNTAX</span></span>

### <span data-ttu-id="bf8c6-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf8c6-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bf8c6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bf8c6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf8c6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bf8c6-107">DESCRIPTION</span></span>
<span data-ttu-id="bf8c6-108">Művelet egy meglévő CommunicationService frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="bf8c6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-109">EXAMPLES</span></span>

### <span data-ttu-id="bf8c6-110">1. példa: Meglévő ACS-erőforrás frissítése címkékkel</span><span class="sxs-lookup"><span data-stu-id="bf8c6-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="bf8c6-111">A megadott címkéket a megadott ACS-erőforráshoz csatolja.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="bf8c6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf8c6-112">PARAMETERS</span></span>

### <span data-ttu-id="bf8c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf8c6-113">-DefaultProfile</span></span>
<span data-ttu-id="bf8c6-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf8c6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf8c6-115">-InputObject</span></span>
<span data-ttu-id="bf8c6-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf8c6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bf8c6-117">-Name</span></span>
<span data-ttu-id="bf8c6-118">A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8c6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf8c6-119">-ResourceGroupName</span></span>
<span data-ttu-id="bf8c6-120">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bf8c6-121">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8c6-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf8c6-122">-SubscriptionId</span></span>
<span data-ttu-id="bf8c6-123">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf8c6-124">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-124">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8c6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf8c6-125">-Tag</span></span>
<span data-ttu-id="bf8c6-126">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcsérték-párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8c6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf8c6-127">-Confirm</span></span>
<span data-ttu-id="bf8c6-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf8c6-129">-WhatIf</span></span>
<span data-ttu-id="bf8c6-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf8c6-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8c6-132">CommonParameters</span></span>
<span data-ttu-id="bf8c6-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8c6-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf8c6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8c6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf8c6-135">INPUTS</span></span>

### <span data-ttu-id="bf8c6-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="bf8c6-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="bf8c6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-137">OUTPUTS</span></span>

### <span data-ttu-id="bf8c6-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="bf8c6-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="bf8c6-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-139">NOTES</span></span>

<span data-ttu-id="bf8c6-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-140">ALIASES</span></span>

<span data-ttu-id="bf8c6-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="bf8c6-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf8c6-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf8c6-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf8c6-144">INPUTOBJECT: <ICommunicationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="bf8c6-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf8c6-145">`[CommunicationServiceName <String>]`: A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="bf8c6-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="bf8c6-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf8c6-147">`[Location <String>]`: Az Azure régió</span><span class="sxs-lookup"><span data-stu-id="bf8c6-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="bf8c6-148">`[OperationId <String>]`: Folyamatban lévő async-művelet azonosítója</span><span class="sxs-lookup"><span data-stu-id="bf8c6-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="bf8c6-149">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bf8c6-150">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bf8c6-151">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="bf8c6-152">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bf8c6-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-153">RELATED LINKS</span></span>

