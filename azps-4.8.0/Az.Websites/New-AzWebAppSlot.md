---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182010"
---
# <span data-ttu-id="45460-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45460-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="45460-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45460-102">SYNOPSIS</span></span>
<span data-ttu-id="45460-103">Azure Web App-bővítőhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="45460-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="45460-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45460-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45460-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45460-105">DESCRIPTION</span></span>
<span data-ttu-id="45460-106">A **New-AzWebAppSlot** parancsmag létrehoz egy Azure Web App-tárolóhelyet egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="45460-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="45460-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45460-107">EXAMPLES</span></span>

### <span data-ttu-id="45460-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45460-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="45460-109">A parancs egy Slot001 nevű bővítőhelyet hoz létre egy meglévő, a ContosoSite nevű, Default-Web-WestUS nevű erőforráscsoport-az Data Center West US-ben.</span><span class="sxs-lookup"><span data-stu-id="45460-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="45460-110">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="45460-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="45460-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45460-111">PARAMETERS</span></span>

### <span data-ttu-id="45460-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="45460-112">-AppServicePlan</span></span>
<span data-ttu-id="45460-113">Alkalmazás-szolgáltatási terv neve vagy alkalmazás-szolgáltatási terv azonosítója. Ha a bővítőhely és az App szolgáltatás terve különböző erőforráscsoport, a név helyett használja az azonosítót.</span><span class="sxs-lookup"><span data-stu-id="45460-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="45460-114">Az alkalmazás-szolgáltatási terv azonosítóját a következő használatával lehet beolvasni: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. id az App Service Plan azonosítóját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="45460-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="45460-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="45460-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="45460-116">Az app beállításai felülírják a Hashtable</span><span class="sxs-lookup"><span data-stu-id="45460-116">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="45460-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="45460-117">-AseName</span></span>
<span data-ttu-id="45460-118">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="45460-118">App Service Environment Name</span></span>

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

### <span data-ttu-id="45460-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45460-119">-AseResourceGroupName</span></span>
<span data-ttu-id="45460-120">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="45460-120">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="45460-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45460-121">-AsJob</span></span>
<span data-ttu-id="45460-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="45460-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45460-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="45460-123">-ContainerImageName</span></span>
<span data-ttu-id="45460-124">Tároló képnév és választható címke (például kép: címke)</span><span class="sxs-lookup"><span data-stu-id="45460-124">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="45460-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="45460-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="45460-126">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="45460-126">Private Container Registry Password</span></span>

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

### <span data-ttu-id="45460-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="45460-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="45460-128">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="45460-128">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="45460-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="45460-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="45460-130">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="45460-130">Private Container Registry Username</span></span>

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

### <span data-ttu-id="45460-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45460-131">-DefaultProfile</span></span>
<span data-ttu-id="45460-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45460-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45460-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="45460-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="45460-134">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="45460-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="45460-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="45460-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="45460-136">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="45460-136">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="45460-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="45460-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="45460-138">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="45460-138">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="45460-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45460-139">-Name</span></span>
<span data-ttu-id="45460-140">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="45460-140">Webapp Name</span></span>

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

### <span data-ttu-id="45460-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45460-141">-ResourceGroupName</span></span>
<span data-ttu-id="45460-142">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="45460-142">Resource Group Name</span></span>

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

### <span data-ttu-id="45460-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="45460-143">-Slot</span></span>
<span data-ttu-id="45460-144">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="45460-144">Webapp Slot Name</span></span>

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

### <span data-ttu-id="45460-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="45460-145">-SourceWebApp</span></span>
<span data-ttu-id="45460-146">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="45460-146">Source WebApp Object</span></span>

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

### <span data-ttu-id="45460-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45460-147">CommonParameters</span></span>
<span data-ttu-id="45460-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45460-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45460-149">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45460-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45460-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45460-150">INPUTS</span></span>

### <span data-ttu-id="45460-151">System. String</span><span class="sxs-lookup"><span data-stu-id="45460-151">System.String</span></span>

### <span data-ttu-id="45460-152">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="45460-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="45460-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45460-153">OUTPUTS</span></span>

### <span data-ttu-id="45460-154">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="45460-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="45460-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45460-155">NOTES</span></span>

## <span data-ttu-id="45460-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45460-156">RELATED LINKS</span></span>

[<span data-ttu-id="45460-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45460-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="45460-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45460-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="45460-159">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45460-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="45460-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45460-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="45460-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45460-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="45460-162">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45460-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="45460-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="45460-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="45460-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="45460-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
