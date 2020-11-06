---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493803"
---
# <span data-ttu-id="2aaeb-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2aaeb-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="2aaeb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2aaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="2aaeb-103">Azure-alkalmazási szolgáltatási csomagot állít be.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aaeb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2aaeb-104">SYNTAX</span></span>

### <span data-ttu-id="2aaeb-105">S1</span><span class="sxs-lookup"><span data-stu-id="2aaeb-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aaeb-106">S2</span><span class="sxs-lookup"><span data-stu-id="2aaeb-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2aaeb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2aaeb-107">DESCRIPTION</span></span>
<span data-ttu-id="2aaeb-108">A **set-AzureRmAppServicePlan** parancsmag az Azure app szolgáltatási csomagját állítja be.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="2aaeb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2aaeb-109">EXAMPLES</span></span>

### <span data-ttu-id="2aaeb-110">1: alkalmazás-szolgáltatási csomag módosítása</span><span class="sxs-lookup"><span data-stu-id="2aaeb-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="2aaeb-111">Ez a parancs beállítja a PerSiteScaling beállítást az ContosoASP nevű app-szolgáltatási tervben, amely a Default-Web-WestUS nevű erőforráscsoport része.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2aaeb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2aaeb-112">PARAMETERS</span></span>

### <span data-ttu-id="2aaeb-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="2aaeb-113">-AdminSiteName</span></span>
<span data-ttu-id="2aaeb-114">Rendszergazdai webhely neve</span><span class="sxs-lookup"><span data-stu-id="2aaeb-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaeb-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2aaeb-115">-AppServicePlan</span></span>
<span data-ttu-id="2aaeb-116">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="2aaeb-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaeb-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2aaeb-117">-Name</span></span>
<span data-ttu-id="2aaeb-118">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="2aaeb-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaeb-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="2aaeb-119">-NumberofWorkers</span></span>
<span data-ttu-id="2aaeb-120">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="2aaeb-120">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaeb-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="2aaeb-121">-PerSiteScaling</span></span>
<span data-ttu-id="2aaeb-122">Egy webhely méretezése logikai értékkel</span><span class="sxs-lookup"><span data-stu-id="2aaeb-122">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaeb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aaeb-123">-ResourceGroupName</span></span>
<span data-ttu-id="2aaeb-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2aaeb-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaeb-125">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="2aaeb-125">-Tier</span></span>
<span data-ttu-id="2aaeb-126">Tier</span><span class="sxs-lookup"><span data-stu-id="2aaeb-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaeb-127">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="2aaeb-127">-WorkerSize</span></span>
<span data-ttu-id="2aaeb-128">Munkatársi méret</span><span class="sxs-lookup"><span data-stu-id="2aaeb-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaeb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaeb-129">-DefaultProfile</span></span>
<span data-ttu-id="2aaeb-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aaeb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaeb-131">CommonParameters</span></span>
<span data-ttu-id="2aaeb-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2aaeb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaeb-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aaeb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaeb-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2aaeb-134">INPUTS</span></span>

### <span data-ttu-id="2aaeb-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2aaeb-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="2aaeb-136">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2aaeb-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="2aaeb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2aaeb-137">OUTPUTS</span></span>

### <span data-ttu-id="2aaeb-138">Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2aaeb-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="2aaeb-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2aaeb-139">NOTES</span></span>

## <span data-ttu-id="2aaeb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2aaeb-140">RELATED LINKS</span></span>

[<span data-ttu-id="2aaeb-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2aaeb-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="2aaeb-142">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2aaeb-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="2aaeb-143">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2aaeb-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="2aaeb-144">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2aaeb-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="2aaeb-145">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2aaeb-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="2aaeb-146">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2aaeb-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


