---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 41851c1492c3c14e3129ba04367580b09cf3ffb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842718"
---
# <span data-ttu-id="cf843-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cf843-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="cf843-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf843-102">SYNOPSIS</span></span>
<span data-ttu-id="cf843-103">Azure Web App-bővítőhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cf843-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="cf843-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf843-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf843-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf843-105">DESCRIPTION</span></span>
<span data-ttu-id="cf843-106">A **New-AzWebAppSlot** parancsmag létrehoz egy Azure Web App-tárolóhelyet egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="cf843-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="cf843-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf843-107">EXAMPLES</span></span>

### <span data-ttu-id="cf843-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf843-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="cf843-109">A parancs egy Slot001 nevű bővítőhelyet hoz létre egy meglévő, a ContosoSite nevű, Default-Web-WestUS nevű erőforráscsoport-az Data Center West US-ben.</span><span class="sxs-lookup"><span data-stu-id="cf843-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="cf843-110">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="cf843-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="cf843-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf843-111">PARAMETERS</span></span>

### <span data-ttu-id="cf843-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cf843-112">-AppServicePlan</span></span>
<span data-ttu-id="cf843-113">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="cf843-113">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="cf843-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="cf843-115">Az app beállításai felülírják a Hashtable</span><span class="sxs-lookup"><span data-stu-id="cf843-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="cf843-116">-AseName</span></span>
<span data-ttu-id="cf843-117">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="cf843-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf843-118">-AseResourceGroupName</span></span>
<span data-ttu-id="cf843-119">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="cf843-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf843-120">-DefaultProfile</span></span>
<span data-ttu-id="cf843-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf843-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="cf843-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="cf843-123">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="cf843-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="cf843-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="cf843-125">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="cf843-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf843-126">-Name</span></span>
<span data-ttu-id="cf843-127">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="cf843-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf843-128">-ResourceGroupName</span></span>
<span data-ttu-id="cf843-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="cf843-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="cf843-130">-Slot</span></span>
<span data-ttu-id="cf843-131">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="cf843-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="cf843-132">-SourceWebApp</span></span>
<span data-ttu-id="cf843-133">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="cf843-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf843-134">-AsJob</span></span>
<span data-ttu-id="cf843-135">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cf843-135">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf843-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf843-136">CommonParameters</span></span>
<span data-ttu-id="cf843-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf843-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf843-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf843-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf843-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf843-139">INPUTS</span></span>

### <span data-ttu-id="cf843-140">Webhely</span><span class="sxs-lookup"><span data-stu-id="cf843-140">Site</span></span>
<span data-ttu-id="cf843-141">A ' SourceWebApp ' paraméter a "webhely" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cf843-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cf843-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf843-142">OUTPUTS</span></span>

## <span data-ttu-id="cf843-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf843-143">NOTES</span></span>

## <span data-ttu-id="cf843-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf843-144">RELATED LINKS</span></span>

[<span data-ttu-id="cf843-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cf843-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="cf843-146">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cf843-146">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="cf843-147">Újraindítás – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cf843-147">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="cf843-148">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cf843-148">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="cf843-149">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cf843-149">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="cf843-150">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cf843-150">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="cf843-151">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cf843-151">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="cf843-152">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cf843-152">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
