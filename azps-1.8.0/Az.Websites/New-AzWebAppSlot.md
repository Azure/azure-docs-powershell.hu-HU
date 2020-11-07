---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668325"
---
# <span data-ttu-id="74a03-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74a03-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="74a03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74a03-102">SYNOPSIS</span></span>
<span data-ttu-id="74a03-103">Azure Web App-bővítőhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="74a03-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="74a03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74a03-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74a03-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="74a03-105">DESCRIPTION</span></span>
<span data-ttu-id="74a03-106">A **New-AzWebAppSlot** parancsmag létrehoz egy Azure Web App-tárolóhelyet egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="74a03-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="74a03-107">Példák</span><span class="sxs-lookup"><span data-stu-id="74a03-107">EXAMPLES</span></span>

### <span data-ttu-id="74a03-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="74a03-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="74a03-109">A parancs egy Slot001 nevű bővítőhelyet hoz létre egy meglévő, a ContosoSite nevű, Default-Web-WestUS nevű erőforráscsoport-az Data Center West US-ben.</span><span class="sxs-lookup"><span data-stu-id="74a03-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="74a03-110">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="74a03-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="74a03-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74a03-111">PARAMETERS</span></span>

### <span data-ttu-id="74a03-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="74a03-112">-AppServicePlan</span></span>
<span data-ttu-id="74a03-113">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="74a03-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="74a03-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="74a03-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="74a03-115">Az app beállításai felülírják a Hashtable</span><span class="sxs-lookup"><span data-stu-id="74a03-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="74a03-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="74a03-116">-AseName</span></span>
<span data-ttu-id="74a03-117">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="74a03-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="74a03-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a03-118">-AseResourceGroupName</span></span>
<span data-ttu-id="74a03-119">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="74a03-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="74a03-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74a03-120">-AsJob</span></span>
<span data-ttu-id="74a03-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="74a03-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74a03-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="74a03-122">-ContainerImageName</span></span>
<span data-ttu-id="74a03-123">Tároló képnév és választható címke (például kép: címke)</span><span class="sxs-lookup"><span data-stu-id="74a03-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="74a03-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="74a03-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="74a03-125">Privát tároló rendszerleíróadatbázis-jelszava</span><span class="sxs-lookup"><span data-stu-id="74a03-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="74a03-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="74a03-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="74a03-127">Privát tároló rendszerleíróadatbázis-kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="74a03-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="74a03-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="74a03-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="74a03-129">Privát tároló rendszerleíróadatbázis-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="74a03-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="74a03-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a03-130">-DefaultProfile</span></span>
<span data-ttu-id="74a03-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74a03-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74a03-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="74a03-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="74a03-133">A tároló folyamatos telepítő webakasztójának engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="74a03-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="74a03-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="74a03-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="74a03-135">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="74a03-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="74a03-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="74a03-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="74a03-137">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="74a03-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="74a03-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74a03-138">-Name</span></span>
<span data-ttu-id="74a03-139">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="74a03-139">Webapp Name</span></span>

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

### <span data-ttu-id="74a03-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a03-140">-ResourceGroupName</span></span>
<span data-ttu-id="74a03-141">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="74a03-141">Resource Group Name</span></span>

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

### <span data-ttu-id="74a03-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="74a03-142">-Slot</span></span>
<span data-ttu-id="74a03-143">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="74a03-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="74a03-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="74a03-144">-SourceWebApp</span></span>
<span data-ttu-id="74a03-145">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="74a03-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="74a03-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a03-146">CommonParameters</span></span>
<span data-ttu-id="74a03-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74a03-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a03-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a03-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a03-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74a03-149">INPUTS</span></span>

### <span data-ttu-id="74a03-150">System. String</span><span class="sxs-lookup"><span data-stu-id="74a03-150">System.String</span></span>

### <span data-ttu-id="74a03-151">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="74a03-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="74a03-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74a03-152">OUTPUTS</span></span>

### <span data-ttu-id="74a03-153">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="74a03-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="74a03-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74a03-154">NOTES</span></span>

## <span data-ttu-id="74a03-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74a03-155">RELATED LINKS</span></span>

[<span data-ttu-id="74a03-156">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74a03-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="74a03-157">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74a03-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="74a03-158">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74a03-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="74a03-159">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74a03-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="74a03-160">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74a03-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="74a03-161">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74a03-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="74a03-162">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="74a03-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="74a03-163">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="74a03-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
