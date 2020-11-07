---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: eac153c22a576686feb15b75f3180ed4fb12ec94
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850186"
---
# <span data-ttu-id="04431-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="04431-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="04431-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04431-102">SYNOPSIS</span></span>
<span data-ttu-id="04431-103">Azure-alkalmazási szolgáltatási csomagot állít be.</span><span class="sxs-lookup"><span data-stu-id="04431-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04431-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04431-104">SYNTAX</span></span>

### <span data-ttu-id="04431-105">S1</span><span class="sxs-lookup"><span data-stu-id="04431-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04431-106">S2</span><span class="sxs-lookup"><span data-stu-id="04431-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04431-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="04431-107">DESCRIPTION</span></span>
<span data-ttu-id="04431-108">A **set-AzureRmAppServicePlan** parancsmag az Azure app szolgáltatási csomagját állítja be.</span><span class="sxs-lookup"><span data-stu-id="04431-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="04431-109">Példák</span><span class="sxs-lookup"><span data-stu-id="04431-109">EXAMPLES</span></span>

### <span data-ttu-id="04431-110">1: alkalmazás-szolgáltatási csomag módosítása</span><span class="sxs-lookup"><span data-stu-id="04431-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="04431-111">Ez a parancs beállítja a PerSiteScaling beállítást az ContosoASP nevű app-szolgáltatási tervben, amely a Default-Web-WestUS nevű erőforráscsoport része.</span><span class="sxs-lookup"><span data-stu-id="04431-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="04431-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04431-112">PARAMETERS</span></span>

### <span data-ttu-id="04431-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="04431-113">-AdminSiteName</span></span>
<span data-ttu-id="04431-114">Rendszergazdai webhely neve</span><span class="sxs-lookup"><span data-stu-id="04431-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04431-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="04431-115">-AppServicePlan</span></span>
<span data-ttu-id="04431-116">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="04431-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04431-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04431-117">-DefaultProfile</span></span>
<span data-ttu-id="04431-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04431-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04431-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04431-119">-Name</span></span>
<span data-ttu-id="04431-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="04431-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04431-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="04431-121">-NumberofWorkers</span></span>
<span data-ttu-id="04431-122">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="04431-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04431-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="04431-123">-PerSiteScaling</span></span>
<span data-ttu-id="04431-124">Egy webhely méretezése logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="04431-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04431-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04431-125">-ResourceGroupName</span></span>
<span data-ttu-id="04431-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="04431-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04431-127">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="04431-127">-Tier</span></span>
<span data-ttu-id="04431-128">Tier</span><span class="sxs-lookup"><span data-stu-id="04431-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04431-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="04431-129">-WorkerSize</span></span>
<span data-ttu-id="04431-130">Munkatársi méret</span><span class="sxs-lookup"><span data-stu-id="04431-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="04431-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04431-131">-AsJob</span></span>
<span data-ttu-id="04431-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="04431-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04431-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04431-133">CommonParameters</span></span>
<span data-ttu-id="04431-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04431-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04431-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04431-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04431-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04431-136">INPUTS</span></span>

### <span data-ttu-id="04431-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="04431-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="04431-138">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="04431-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="04431-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04431-139">OUTPUTS</span></span>

### <span data-ttu-id="04431-140">Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="04431-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="04431-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04431-141">NOTES</span></span>

## <span data-ttu-id="04431-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04431-142">RELATED LINKS</span></span>

[<span data-ttu-id="04431-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="04431-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="04431-144">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="04431-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="04431-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="04431-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="04431-146">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="04431-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="04431-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="04431-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="04431-148">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="04431-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


