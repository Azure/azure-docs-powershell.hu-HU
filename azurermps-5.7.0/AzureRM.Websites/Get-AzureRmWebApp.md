---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 55bce35d7aa0cc3c2cff905020159f9ba204a48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501295"
---
# <span data-ttu-id="0066c-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0066c-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="0066c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0066c-102">SYNOPSIS</span></span>
<span data-ttu-id="0066c-103">A megadott erőforráscsoport Azure Web Apps-t kap.</span><span class="sxs-lookup"><span data-stu-id="0066c-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0066c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0066c-104">SYNTAX</span></span>

### <span data-ttu-id="0066c-105">S1</span><span class="sxs-lookup"><span data-stu-id="0066c-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0066c-106">S2</span><span class="sxs-lookup"><span data-stu-id="0066c-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0066c-107">S3</span><span class="sxs-lookup"><span data-stu-id="0066c-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0066c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0066c-108">DESCRIPTION</span></span>
<span data-ttu-id="0066c-109">A **Get-AzureRmWebApp** parancsmag információkat kap az Azure Web App alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="0066c-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="0066c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0066c-110">EXAMPLES</span></span>

### <span data-ttu-id="0066c-111">Példa 1: webalkalmazás beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="0066c-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="0066c-112">Ez a parancs beilleszti a ContosoSite nevű webalkalmazást, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="0066c-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0066c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0066c-113">PARAMETERS</span></span>

### <span data-ttu-id="0066c-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0066c-114">-AppServicePlan</span></span>
<span data-ttu-id="0066c-115">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="0066c-115">App Service Plan object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0066c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0066c-116">-DefaultProfile</span></span>
<span data-ttu-id="0066c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0066c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0066c-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="0066c-118">-Location</span></span>
<span data-ttu-id="0066c-119">Helyre</span><span class="sxs-lookup"><span data-stu-id="0066c-119">Location</span></span>

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

### <span data-ttu-id="0066c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0066c-120">-Name</span></span>
<span data-ttu-id="0066c-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="0066c-121">WebApp Name</span></span>

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

### <span data-ttu-id="0066c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0066c-122">-ResourceGroupName</span></span>
<span data-ttu-id="0066c-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0066c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0066c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0066c-124">CommonParameters</span></span>
<span data-ttu-id="0066c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0066c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0066c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0066c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0066c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0066c-127">INPUTS</span></span>

### <span data-ttu-id="0066c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0066c-128">System.String</span></span>

## <span data-ttu-id="0066c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0066c-129">OUTPUTS</span></span>

### <span data-ttu-id="0066c-130">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="0066c-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="0066c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0066c-131">NOTES</span></span>

## <span data-ttu-id="0066c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0066c-132">RELATED LINKS</span></span>

[<span data-ttu-id="0066c-133">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0066c-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="0066c-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0066c-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0066c-135">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0066c-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0066c-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0066c-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="0066c-137">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0066c-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


