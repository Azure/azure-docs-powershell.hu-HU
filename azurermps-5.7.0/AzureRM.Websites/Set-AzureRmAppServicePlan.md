---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 16b2c8df737047619366ebf6b75a4c2ed2264fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501283"
---
# <span data-ttu-id="b2731-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2731-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="b2731-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2731-102">SYNOPSIS</span></span>
<span data-ttu-id="b2731-103">Azure-alkalmazási szolgáltatási csomagot állít be.</span><span class="sxs-lookup"><span data-stu-id="b2731-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2731-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2731-104">SYNTAX</span></span>

### <span data-ttu-id="b2731-105">S1</span><span class="sxs-lookup"><span data-stu-id="b2731-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2731-106">S2</span><span class="sxs-lookup"><span data-stu-id="b2731-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2731-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2731-107">DESCRIPTION</span></span>
<span data-ttu-id="b2731-108">A **set-AzureRmAppServicePlan** parancsmag az Azure app szolgáltatási csomagját állítja be.</span><span class="sxs-lookup"><span data-stu-id="b2731-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="b2731-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b2731-109">EXAMPLES</span></span>

### <span data-ttu-id="b2731-110">1: alkalmazás-szolgáltatási csomag módosítása</span><span class="sxs-lookup"><span data-stu-id="b2731-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="b2731-111">Ez a parancs beállítja a PerSiteScaling beállítást az ContosoASP nevű app-szolgáltatási tervben, amely a Default-Web-WestUS nevű erőforráscsoport része.</span><span class="sxs-lookup"><span data-stu-id="b2731-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b2731-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2731-112">PARAMETERS</span></span>

### <span data-ttu-id="b2731-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="b2731-113">-AdminSiteName</span></span>
<span data-ttu-id="b2731-114">Rendszergazdai webhely neve</span><span class="sxs-lookup"><span data-stu-id="b2731-114">Admin Site Name</span></span>

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

### <span data-ttu-id="b2731-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2731-115">-AppServicePlan</span></span>
<span data-ttu-id="b2731-116">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="b2731-116">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2731-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2731-117">-DefaultProfile</span></span>
<span data-ttu-id="b2731-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2731-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2731-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2731-119">-Name</span></span>
<span data-ttu-id="b2731-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="b2731-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="b2731-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="b2731-121">-NumberofWorkers</span></span>
<span data-ttu-id="b2731-122">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="b2731-122">Number Of Workers</span></span>

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

### <span data-ttu-id="b2731-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="b2731-123">-PerSiteScaling</span></span>
<span data-ttu-id="b2731-124">Egy webhely méretezése logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="b2731-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="b2731-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2731-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2731-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b2731-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b2731-127">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="b2731-127">-Tier</span></span>
<span data-ttu-id="b2731-128">Tier</span><span class="sxs-lookup"><span data-stu-id="b2731-128">Tier</span></span>

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

### <span data-ttu-id="b2731-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="b2731-129">-WorkerSize</span></span>
<span data-ttu-id="b2731-130">Munkatársi méret</span><span class="sxs-lookup"><span data-stu-id="b2731-130">Worker Size</span></span>

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
### <span data-ttu-id="b2731-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2731-131">-AsJob</span></span>
<span data-ttu-id="b2731-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b2731-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2731-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2731-133">CommonParameters</span></span>
<span data-ttu-id="b2731-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2731-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2731-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2731-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2731-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2731-136">INPUTS</span></span>

### <span data-ttu-id="b2731-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b2731-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="b2731-138">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b2731-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="b2731-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2731-139">OUTPUTS</span></span>

### <span data-ttu-id="b2731-140">Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b2731-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="b2731-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2731-141">NOTES</span></span>

## <span data-ttu-id="b2731-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2731-142">RELATED LINKS</span></span>

[<span data-ttu-id="b2731-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2731-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="b2731-144">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2731-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="b2731-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2731-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="b2731-146">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2731-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="b2731-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2731-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="b2731-148">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2731-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


