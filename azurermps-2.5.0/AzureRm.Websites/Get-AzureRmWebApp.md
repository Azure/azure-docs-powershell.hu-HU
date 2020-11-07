---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848058"
---
# <span data-ttu-id="e8598-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8598-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="e8598-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8598-102">SYNOPSIS</span></span>
<span data-ttu-id="e8598-103">A megadott erőforráscsoport Azure Web Apps-t kap.</span><span class="sxs-lookup"><span data-stu-id="e8598-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8598-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8598-104">SYNTAX</span></span>

### <span data-ttu-id="e8598-105">S1</span><span class="sxs-lookup"><span data-stu-id="e8598-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8598-106">S2</span><span class="sxs-lookup"><span data-stu-id="e8598-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8598-107">S3</span><span class="sxs-lookup"><span data-stu-id="e8598-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8598-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8598-108">DESCRIPTION</span></span>
<span data-ttu-id="e8598-109">A **Get-AzureRmWebApp** parancsmag információkat kap az Azure Web App alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="e8598-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="e8598-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e8598-110">EXAMPLES</span></span>

### <span data-ttu-id="e8598-111">Példa 1: webalkalmazás beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="e8598-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e8598-112">Ez a parancs beilleszti a ContosoSite nevű webalkalmazást, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="e8598-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e8598-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8598-113">PARAMETERS</span></span>

### <span data-ttu-id="e8598-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e8598-114">-AppServicePlan</span></span>
<span data-ttu-id="e8598-115">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="e8598-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8598-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8598-116">-DefaultProfile</span></span>
<span data-ttu-id="e8598-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8598-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8598-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="e8598-118">-Location</span></span>
<span data-ttu-id="e8598-119">Helyre</span><span class="sxs-lookup"><span data-stu-id="e8598-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8598-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8598-120">-Name</span></span>
<span data-ttu-id="e8598-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e8598-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8598-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8598-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8598-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e8598-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8598-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8598-124">CommonParameters</span></span>
<span data-ttu-id="e8598-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8598-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8598-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8598-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8598-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8598-127">INPUTS</span></span>

### <span data-ttu-id="e8598-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e8598-128">System.String</span></span>

## <span data-ttu-id="e8598-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8598-129">OUTPUTS</span></span>

### <span data-ttu-id="e8598-130">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="e8598-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="e8598-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8598-131">NOTES</span></span>

## <span data-ttu-id="e8598-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8598-132">RELATED LINKS</span></span>

[<span data-ttu-id="e8598-133">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8598-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="e8598-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8598-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="e8598-135">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8598-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="e8598-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8598-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="e8598-137">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8598-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


