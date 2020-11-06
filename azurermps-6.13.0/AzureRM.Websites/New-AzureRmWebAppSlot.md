---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502792"
---
# <span data-ttu-id="f958f-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f958f-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="f958f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f958f-102">SYNOPSIS</span></span>
<span data-ttu-id="f958f-103">Azure Web App-bővítőhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f958f-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f958f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f958f-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f958f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f958f-105">DESCRIPTION</span></span>
<span data-ttu-id="f958f-106">A **New-AzureRmWebAppSlot** parancsmag létrehoz egy Azure Web App-tárolóhelyet egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="f958f-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="f958f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f958f-107">EXAMPLES</span></span>

### <span data-ttu-id="f958f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f958f-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="f958f-109">A parancs egy Slot001 nevű bővítőhelyet hoz létre egy meglévő, a ContosoSite nevű, Default-Web-WestUS nevű erőforráscsoport-az Data Center West US-ben.</span><span class="sxs-lookup"><span data-stu-id="f958f-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="f958f-110">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="f958f-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="f958f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f958f-111">PARAMETERS</span></span>

### <span data-ttu-id="f958f-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f958f-112">-AppServicePlan</span></span>
<span data-ttu-id="f958f-113">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="f958f-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="f958f-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="f958f-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="f958f-115">Az app beállításai felülírják a Hashtable</span><span class="sxs-lookup"><span data-stu-id="f958f-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="f958f-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="f958f-116">-AseName</span></span>
<span data-ttu-id="f958f-117">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="f958f-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="f958f-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f958f-118">-AseResourceGroupName</span></span>
<span data-ttu-id="f958f-119">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="f958f-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="f958f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f958f-120">-AsJob</span></span>
<span data-ttu-id="f958f-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f958f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f958f-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="f958f-122">-ContainerImageName</span></span>
<span data-ttu-id="f958f-123">Tároló képnév és választható címke (például kép: címke)</span><span class="sxs-lookup"><span data-stu-id="f958f-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="f958f-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="f958f-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="f958f-125">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="f958f-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="f958f-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="f958f-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="f958f-127">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="f958f-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="f958f-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="f958f-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="f958f-129">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="f958f-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="f958f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f958f-130">-DefaultProfile</span></span>
<span data-ttu-id="f958f-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f958f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f958f-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="f958f-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="f958f-133">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="f958f-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="f958f-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="f958f-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="f958f-135">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="f958f-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="f958f-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="f958f-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="f958f-137">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="f958f-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="f958f-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f958f-138">-Name</span></span>
<span data-ttu-id="f958f-139">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f958f-139">Webapp Name</span></span>

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

### <span data-ttu-id="f958f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f958f-140">-ResourceGroupName</span></span>
<span data-ttu-id="f958f-141">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f958f-141">Resource Group Name</span></span>

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

### <span data-ttu-id="f958f-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="f958f-142">-Slot</span></span>
<span data-ttu-id="f958f-143">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="f958f-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="f958f-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="f958f-144">-SourceWebApp</span></span>
<span data-ttu-id="f958f-145">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="f958f-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="f958f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f958f-146">CommonParameters</span></span>
<span data-ttu-id="f958f-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f958f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f958f-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f958f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f958f-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f958f-149">INPUTS</span></span>

### <span data-ttu-id="f958f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f958f-150">System.String</span></span>

### <span data-ttu-id="f958f-151">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="f958f-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="f958f-152">Paraméterek: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f958f-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="f958f-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f958f-153">OUTPUTS</span></span>

### <span data-ttu-id="f958f-154">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="f958f-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="f958f-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f958f-155">NOTES</span></span>

## <span data-ttu-id="f958f-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f958f-156">RELATED LINKS</span></span>

[<span data-ttu-id="f958f-157">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f958f-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="f958f-158">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f958f-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="f958f-159">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f958f-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="f958f-160">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f958f-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="f958f-161">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f958f-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="f958f-162">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f958f-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="f958f-163">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f958f-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="f958f-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f958f-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
