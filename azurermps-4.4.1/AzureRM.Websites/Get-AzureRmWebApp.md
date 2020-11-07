---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673076"
---
# <span data-ttu-id="80b76-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="80b76-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="80b76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80b76-102">SYNOPSIS</span></span>
<span data-ttu-id="80b76-103">A megadott erőforráscsoport Azure Web Apps-t kap.</span><span class="sxs-lookup"><span data-stu-id="80b76-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80b76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80b76-104">SYNTAX</span></span>

### <span data-ttu-id="80b76-105">S1</span><span class="sxs-lookup"><span data-stu-id="80b76-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80b76-106">S2</span><span class="sxs-lookup"><span data-stu-id="80b76-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80b76-107">S3</span><span class="sxs-lookup"><span data-stu-id="80b76-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80b76-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="80b76-108">DESCRIPTION</span></span>
<span data-ttu-id="80b76-109">A **Get-AzureRmWebApp** parancsmag információkat kap az Azure Web App alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="80b76-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="80b76-110">Példák</span><span class="sxs-lookup"><span data-stu-id="80b76-110">EXAMPLES</span></span>

### <span data-ttu-id="80b76-111">Példa 1: webalkalmazás beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="80b76-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="80b76-112">Ez a parancs beilleszti a ContosoSite nevű webalkalmazást, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="80b76-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="80b76-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80b76-113">PARAMETERS</span></span>

### <span data-ttu-id="80b76-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="80b76-114">-AppServicePlan</span></span>
<span data-ttu-id="80b76-115">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="80b76-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b76-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="80b76-116">-Location</span></span>
<span data-ttu-id="80b76-117">Helyre</span><span class="sxs-lookup"><span data-stu-id="80b76-117">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b76-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80b76-118">-Name</span></span>
<span data-ttu-id="80b76-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="80b76-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b76-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b76-120">-ResourceGroupName</span></span>
<span data-ttu-id="80b76-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="80b76-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b76-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b76-122">-DefaultProfile</span></span>
<span data-ttu-id="80b76-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80b76-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80b76-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b76-124">CommonParameters</span></span>
<span data-ttu-id="80b76-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80b76-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b76-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b76-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b76-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80b76-127">INPUTS</span></span>

## <span data-ttu-id="80b76-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80b76-128">OUTPUTS</span></span>

## <span data-ttu-id="80b76-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80b76-129">NOTES</span></span>

## <span data-ttu-id="80b76-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80b76-130">RELATED LINKS</span></span>

[<span data-ttu-id="80b76-131">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="80b76-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="80b76-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="80b76-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="80b76-133">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="80b76-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="80b76-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="80b76-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="80b76-135">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="80b76-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


