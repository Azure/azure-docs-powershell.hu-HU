---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467000"
---
# <span data-ttu-id="e2678-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e2678-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="e2678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2678-102">SYNOPSIS</span></span>
<span data-ttu-id="e2678-103">Létrehoz egy Azure Web App-helyet.</span><span class="sxs-lookup"><span data-stu-id="e2678-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="e2678-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2678-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2678-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2678-105">DESCRIPTION</span></span>
<span data-ttu-id="e2678-106">A **New-AzWebAppSzaj** parancsmag létrehoz egy Azure Web App Slotot egy adott erőforráscsoportban, amely a megadott appszolgáltatás-tervet és -adatközpontot használja.</span><span class="sxs-lookup"><span data-stu-id="e2678-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="e2678-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2678-107">EXAMPLES</span></span>

### <span data-ttu-id="e2678-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2678-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="e2678-109">Ez a parancs létrehoz egy Slot001 nevű helyet egy ContosoSite nevű meglévő webalkalmazás alatt a Default-Web-WestUS nevű meglévő erőforráscsoportban a Nyugat-USA adatközpontban.</span><span class="sxs-lookup"><span data-stu-id="e2678-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="e2678-110">A parancs egy ContosoServicePlan nevű meglévő appszolgáltatás-tervet használ.</span><span class="sxs-lookup"><span data-stu-id="e2678-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="e2678-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2678-111">PARAMETERS</span></span>

### <span data-ttu-id="e2678-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2678-112">-AppServicePlan</span></span>
<span data-ttu-id="e2678-113">App Service Plan Name or App Service Plan Id. Ha a slot and app service plan are in different Resource Groups, use the ID instead of the name.</span><span class="sxs-lookup"><span data-stu-id="e2678-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="e2678-114">Az appszolgáltatás-azonosító a következő használatával szerezhető be: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id adja vissza az appszolgáltatás-terv azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="e2678-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="e2678-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="e2678-116">App Settings Overrides Hashtable</span><span class="sxs-lookup"><span data-stu-id="e2678-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="e2678-117">-AseName</span></span>
<span data-ttu-id="e2678-118">Appszolgáltatás-környezet neve</span><span class="sxs-lookup"><span data-stu-id="e2678-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2678-119">-AseResourceGroupName</span></span>
<span data-ttu-id="e2678-120">App Service Environment Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="e2678-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2678-121">-AsJob</span></span>
<span data-ttu-id="e2678-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e2678-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="e2678-123">-ContainerImageName</span></span>
<span data-ttu-id="e2678-124">Container Image Name and optional tag, például (image:tag)</span><span class="sxs-lookup"><span data-stu-id="e2678-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="e2678-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="e2678-126">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="e2678-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="e2678-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="e2678-128">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="e2678-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="e2678-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="e2678-130">Private Container Registry Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="e2678-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2678-131">-DefaultProfile</span></span>
<span data-ttu-id="e2678-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2678-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2678-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="e2678-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="e2678-134">Engedélyezi/letiltja a tároló folyamatos üzembe helyezését webhook</span><span class="sxs-lookup"><span data-stu-id="e2678-134">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="e2678-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="e2678-136">Egyéni állomásnevek figyelmen kívül hagyása beállítás</span><span class="sxs-lookup"><span data-stu-id="e2678-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="e2678-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="e2678-138">A Forrásvezérlő mellőzása beállítás</span><span class="sxs-lookup"><span data-stu-id="e2678-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-139">-Name</span><span class="sxs-lookup"><span data-stu-id="e2678-139">-Name</span></span>
<span data-ttu-id="e2678-140">Webapp neve</span><span class="sxs-lookup"><span data-stu-id="e2678-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2678-141">-ResourceGroupName</span></span>
<span data-ttu-id="e2678-142">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e2678-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="e2678-143">-Slot</span></span>
<span data-ttu-id="e2678-144">Webapp Slot Name</span><span class="sxs-lookup"><span data-stu-id="e2678-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="e2678-145">-SourceWebApp</span></span>
<span data-ttu-id="e2678-146">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="e2678-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2678-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2678-147">CommonParameters</span></span>
<span data-ttu-id="e2678-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2678-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2678-149">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2678-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2678-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2678-150">INPUTS</span></span>

### <span data-ttu-id="e2678-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e2678-151">System.String</span></span>

### <span data-ttu-id="e2678-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e2678-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e2678-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2678-153">OUTPUTS</span></span>

### <span data-ttu-id="e2678-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e2678-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e2678-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2678-155">NOTES</span></span>

## <span data-ttu-id="e2678-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2678-156">RELATED LINKS</span></span>

[<span data-ttu-id="e2678-157">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="e2678-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e2678-158">Remove-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="e2678-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="e2678-159">Restart-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="e2678-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="e2678-160">Set-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="e2678-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="e2678-161">Start-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="e2678-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="e2678-162">Stop-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="e2678-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="e2678-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2678-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="e2678-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2678-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
