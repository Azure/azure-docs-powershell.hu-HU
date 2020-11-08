---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183373"
---
# <span data-ttu-id="6d43f-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="6d43f-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="6d43f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d43f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d43f-103">Információ kérése virtuális gép képsablonról</span><span class="sxs-lookup"><span data-stu-id="6d43f-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="6d43f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d43f-104">SYNTAX</span></span>

### <span data-ttu-id="6d43f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d43f-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d43f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6d43f-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d43f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d43f-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d43f-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="6d43f-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6d43f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d43f-109">DESCRIPTION</span></span>
<span data-ttu-id="6d43f-110">Információ kérése virtuális gép képsablonról</span><span class="sxs-lookup"><span data-stu-id="6d43f-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="6d43f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6d43f-111">EXAMPLES</span></span>

### <span data-ttu-id="6d43f-112">Példa 1: az összes sablon listázása az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="6d43f-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="6d43f-113">Ez a parancs az előfizetés alatti összes sablont felsorolja.</span><span class="sxs-lookup"><span data-stu-id="6d43f-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="6d43f-114">2. példa: az összes sablon listázása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="6d43f-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="6d43f-115">Ez a parancs felsorolja az összes, erőforráscsoport alatti sablont.</span><span class="sxs-lookup"><span data-stu-id="6d43f-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="6d43f-116">3. példa: sablon beszerzése erőforráscsoport szerint</span><span class="sxs-lookup"><span data-stu-id="6d43f-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="6d43f-117">Ez a parancs egy erőforráscsoport alatti sablont kap.</span><span class="sxs-lookup"><span data-stu-id="6d43f-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="6d43f-118">Példa 4: az erőforráscsoport alatti sablon beszerzése</span><span class="sxs-lookup"><span data-stu-id="6d43f-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="6d43f-119">Ez a parancs egy erőforráscsoport alatti sablont kap.</span><span class="sxs-lookup"><span data-stu-id="6d43f-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="6d43f-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d43f-120">PARAMETERS</span></span>

### <span data-ttu-id="6d43f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d43f-121">-DefaultProfile</span></span>
<span data-ttu-id="6d43f-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d43f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d43f-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="6d43f-123">-ImageTemplateName</span></span>
<span data-ttu-id="6d43f-124">A Képsablon neve</span><span class="sxs-lookup"><span data-stu-id="6d43f-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d43f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d43f-125">-InputObject</span></span>
<span data-ttu-id="6d43f-126">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d43f-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d43f-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d43f-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d43f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d43f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d43f-129">-SubscriptionId</span></span>
<span data-ttu-id="6d43f-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6d43f-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d43f-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6d43f-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d43f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d43f-132">CommonParameters</span></span>
<span data-ttu-id="6d43f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d43f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d43f-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d43f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d43f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d43f-135">INPUTS</span></span>

### <span data-ttu-id="6d43f-136">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="6d43f-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="6d43f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d43f-137">OUTPUTS</span></span>

### <span data-ttu-id="6d43f-138">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. modellek. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="6d43f-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="6d43f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d43f-139">NOTES</span></span>

<span data-ttu-id="6d43f-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6d43f-140">ALIASES</span></span>

<span data-ttu-id="6d43f-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6d43f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d43f-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6d43f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d43f-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6d43f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d43f-144">INPUTOBJECT <IImageBuilderIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6d43f-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d43f-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6d43f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d43f-146">`[ImageTemplateName <String>]`: A Képsablon neve</span><span class="sxs-lookup"><span data-stu-id="6d43f-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="6d43f-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d43f-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6d43f-148">`[RunOutputName <String>]`: A futtatott kimenet neve</span><span class="sxs-lookup"><span data-stu-id="6d43f-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="6d43f-149">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6d43f-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6d43f-150">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6d43f-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6d43f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d43f-151">RELATED LINKS</span></span>

