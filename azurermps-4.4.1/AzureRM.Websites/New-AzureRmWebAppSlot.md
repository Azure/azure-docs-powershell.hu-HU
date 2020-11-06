---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 3e886803ff608522bd2d563dd9b6cd6effcfe074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504668"
---
# <span data-ttu-id="cae8e-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cae8e-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="cae8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cae8e-102">SYNOPSIS</span></span>
<span data-ttu-id="cae8e-103">Azure Web App-bővítőhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cae8e-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cae8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cae8e-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cae8e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cae8e-105">DESCRIPTION</span></span>
<span data-ttu-id="cae8e-106">A **New-AzureRmWebAppSlot** parancsmag létrehoz egy Azure Web App-tárolóhelyet egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="cae8e-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="cae8e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cae8e-107">EXAMPLES</span></span>

### <span data-ttu-id="cae8e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cae8e-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="cae8e-109">A parancs egy Slot001 nevű bővítőhelyet hoz létre egy meglévő, a ContosoSite nevű, Default-Web-WestUS nevű erőforráscsoport-az Data Center West US-ben.</span><span class="sxs-lookup"><span data-stu-id="cae8e-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="cae8e-110">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="cae8e-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="cae8e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cae8e-111">PARAMETERS</span></span>

### <span data-ttu-id="cae8e-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cae8e-112">-AppServicePlan</span></span>
<span data-ttu-id="cae8e-113">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="cae8e-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="cae8e-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="cae8e-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="cae8e-115">Az app beállításai felülírják a Hashtable</span><span class="sxs-lookup"><span data-stu-id="cae8e-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="cae8e-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="cae8e-116">-AseName</span></span>
<span data-ttu-id="cae8e-117">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="cae8e-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="cae8e-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae8e-118">-AseResourceGroupName</span></span>
<span data-ttu-id="cae8e-119">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="cae8e-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="cae8e-120">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="cae8e-120">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="cae8e-121">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="cae8e-121">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="cae8e-122">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="cae8e-122">-IgnoreSourceControl</span></span>
<span data-ttu-id="cae8e-123">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="cae8e-123">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="cae8e-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cae8e-124">-Name</span></span>
<span data-ttu-id="cae8e-125">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="cae8e-125">Webapp Name</span></span>

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

### <span data-ttu-id="cae8e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae8e-126">-ResourceGroupName</span></span>
<span data-ttu-id="cae8e-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="cae8e-127">Resource Group Name</span></span>

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

### <span data-ttu-id="cae8e-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="cae8e-128">-Slot</span></span>
<span data-ttu-id="cae8e-129">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="cae8e-129">Webapp Slot Name</span></span>

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

### <span data-ttu-id="cae8e-130">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="cae8e-130">-SourceWebApp</span></span>
<span data-ttu-id="cae8e-131">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="cae8e-131">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae8e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae8e-132">-DefaultProfile</span></span>
<span data-ttu-id="cae8e-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cae8e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cae8e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae8e-134">CommonParameters</span></span>
<span data-ttu-id="cae8e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cae8e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae8e-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae8e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae8e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cae8e-137">INPUTS</span></span>

### <span data-ttu-id="cae8e-138">Webhely</span><span class="sxs-lookup"><span data-stu-id="cae8e-138">Site</span></span>
<span data-ttu-id="cae8e-139">A ' SourceWebApp ' paraméter a "webhely" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cae8e-139">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cae8e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cae8e-140">OUTPUTS</span></span>

## <span data-ttu-id="cae8e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cae8e-141">NOTES</span></span>

## <span data-ttu-id="cae8e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cae8e-142">RELATED LINKS</span></span>

[<span data-ttu-id="cae8e-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cae8e-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="cae8e-144">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cae8e-144">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="cae8e-145">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cae8e-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="cae8e-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cae8e-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="cae8e-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cae8e-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="cae8e-148">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cae8e-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="cae8e-149">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cae8e-149">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="cae8e-150">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="cae8e-150">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
