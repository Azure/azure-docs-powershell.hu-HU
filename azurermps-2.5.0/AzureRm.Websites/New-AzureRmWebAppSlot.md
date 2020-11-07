---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: f41149c6abb946340acc06b847c72dcabcee18fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848966"
---
# <span data-ttu-id="48456-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48456-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="48456-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48456-102">SYNOPSIS</span></span>
<span data-ttu-id="48456-103">Azure Web App-bővítőhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="48456-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48456-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48456-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48456-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48456-105">DESCRIPTION</span></span>
<span data-ttu-id="48456-106">A **New-AzureRmWebAppSlot** parancsmag létrehoz egy Azure Web App-tárolóhelyet egy olyan erőforrás-csoportban, amely a megadott app Service Plan és Data Center alkalmazást használja.</span><span class="sxs-lookup"><span data-stu-id="48456-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="48456-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48456-107">EXAMPLES</span></span>

### <span data-ttu-id="48456-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48456-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="48456-109">A parancs egy Slot001 nevű bővítőhelyet hoz létre egy meglévő, a ContosoSite nevű, Default-Web-WestUS nevű erőforráscsoport-az Data Center West US-ben.</span><span class="sxs-lookup"><span data-stu-id="48456-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="48456-110">A parancs a ContosoServicePlan nevű meglévő alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="48456-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="48456-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48456-111">PARAMETERS</span></span>

### <span data-ttu-id="48456-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="48456-112">-AppServicePlan</span></span>
<span data-ttu-id="48456-113">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="48456-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="48456-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="48456-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="48456-115">Az app beállításai felülírják a Hashtable</span><span class="sxs-lookup"><span data-stu-id="48456-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="48456-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="48456-116">-AseName</span></span>
<span data-ttu-id="48456-117">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="48456-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="48456-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48456-118">-AseResourceGroupName</span></span>
<span data-ttu-id="48456-119">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="48456-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="48456-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48456-120">-DefaultProfile</span></span>
<span data-ttu-id="48456-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48456-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48456-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="48456-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="48456-123">Egyéni állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="48456-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="48456-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="48456-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="48456-125">A Forrásobjektum-vezérlő mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="48456-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="48456-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48456-126">-Name</span></span>
<span data-ttu-id="48456-127">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="48456-127">Webapp Name</span></span>

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

### <span data-ttu-id="48456-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48456-128">-ResourceGroupName</span></span>
<span data-ttu-id="48456-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="48456-129">Resource Group Name</span></span>

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

### <span data-ttu-id="48456-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="48456-130">-Slot</span></span>
<span data-ttu-id="48456-131">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="48456-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="48456-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="48456-132">-SourceWebApp</span></span>
<span data-ttu-id="48456-133">Source WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="48456-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="48456-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48456-134">-AsJob</span></span>
<span data-ttu-id="48456-135">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="48456-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48456-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48456-136">CommonParameters</span></span>
<span data-ttu-id="48456-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48456-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48456-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48456-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48456-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48456-139">INPUTS</span></span>

### <span data-ttu-id="48456-140">Webhely</span><span class="sxs-lookup"><span data-stu-id="48456-140">Site</span></span>
<span data-ttu-id="48456-141">A ' SourceWebApp ' paraméter a "webhely" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="48456-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="48456-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48456-142">OUTPUTS</span></span>

## <span data-ttu-id="48456-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48456-143">NOTES</span></span>

## <span data-ttu-id="48456-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48456-144">RELATED LINKS</span></span>

[<span data-ttu-id="48456-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48456-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="48456-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48456-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="48456-147">Újraindítás – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48456-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="48456-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48456-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="48456-149">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48456-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="48456-150">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48456-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="48456-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="48456-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="48456-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="48456-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
