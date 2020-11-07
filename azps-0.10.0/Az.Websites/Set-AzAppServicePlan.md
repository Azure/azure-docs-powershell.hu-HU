---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842681"
---
# <span data-ttu-id="857ad-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="857ad-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="857ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="857ad-102">SYNOPSIS</span></span>
<span data-ttu-id="857ad-103">Azure-alkalmazási szolgáltatási csomagot állít be.</span><span class="sxs-lookup"><span data-stu-id="857ad-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="857ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="857ad-104">SYNTAX</span></span>

### <span data-ttu-id="857ad-105">S1</span><span class="sxs-lookup"><span data-stu-id="857ad-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="857ad-106">S2</span><span class="sxs-lookup"><span data-stu-id="857ad-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="857ad-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="857ad-107">DESCRIPTION</span></span>
<span data-ttu-id="857ad-108">A **set-AzAppServicePlan** parancsmag az Azure app szolgáltatási csomagját állítja be.</span><span class="sxs-lookup"><span data-stu-id="857ad-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="857ad-109">Példák</span><span class="sxs-lookup"><span data-stu-id="857ad-109">EXAMPLES</span></span>

### <span data-ttu-id="857ad-110">1: alkalmazás-szolgáltatási csomag módosítása</span><span class="sxs-lookup"><span data-stu-id="857ad-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="857ad-111">Ez a parancs beállítja a PerSiteScaling beállítást az ContosoASP nevű app-szolgáltatási tervben, amely a Default-Web-WestUS nevű erőforráscsoport része.</span><span class="sxs-lookup"><span data-stu-id="857ad-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="857ad-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="857ad-112">PARAMETERS</span></span>

### <span data-ttu-id="857ad-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="857ad-113">-AdminSiteName</span></span>
<span data-ttu-id="857ad-114">Rendszergazdai webhely neve</span><span class="sxs-lookup"><span data-stu-id="857ad-114">Admin Site Name</span></span>

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

### <span data-ttu-id="857ad-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="857ad-115">-AppServicePlan</span></span>
<span data-ttu-id="857ad-116">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="857ad-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="857ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857ad-117">-DefaultProfile</span></span>
<span data-ttu-id="857ad-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="857ad-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="857ad-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="857ad-119">-Name</span></span>
<span data-ttu-id="857ad-120">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="857ad-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="857ad-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="857ad-121">-NumberofWorkers</span></span>
<span data-ttu-id="857ad-122">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="857ad-122">Number Of Workers</span></span>

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

### <span data-ttu-id="857ad-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="857ad-123">-PerSiteScaling</span></span>
<span data-ttu-id="857ad-124">Egy webhely méretezése logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="857ad-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="857ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="857ad-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="857ad-126">Resource Group Name</span></span>

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

### <span data-ttu-id="857ad-127">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="857ad-127">-Tier</span></span>
<span data-ttu-id="857ad-128">Tier</span><span class="sxs-lookup"><span data-stu-id="857ad-128">Tier</span></span>

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

### <span data-ttu-id="857ad-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="857ad-129">-WorkerSize</span></span>
<span data-ttu-id="857ad-130">Munkatársi méret</span><span class="sxs-lookup"><span data-stu-id="857ad-130">Worker Size</span></span>

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
### <span data-ttu-id="857ad-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="857ad-131">-AsJob</span></span>
<span data-ttu-id="857ad-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="857ad-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="857ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857ad-133">CommonParameters</span></span>
<span data-ttu-id="857ad-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="857ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857ad-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="857ad-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857ad-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="857ad-136">INPUTS</span></span>

### <span data-ttu-id="857ad-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="857ad-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="857ad-138">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="857ad-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="857ad-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="857ad-139">OUTPUTS</span></span>

### <span data-ttu-id="857ad-140">Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="857ad-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="857ad-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="857ad-141">NOTES</span></span>

## <span data-ttu-id="857ad-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="857ad-142">RELATED LINKS</span></span>

[<span data-ttu-id="857ad-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="857ad-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="857ad-144">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="857ad-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="857ad-145">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="857ad-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="857ad-146">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="857ad-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="857ad-147">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="857ad-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="857ad-148">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="857ad-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


