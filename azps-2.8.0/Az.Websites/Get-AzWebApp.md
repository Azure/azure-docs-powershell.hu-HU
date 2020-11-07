---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: d1217f3abc00fec8752fcddbb30e577df087b5de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837005"
---
# <span data-ttu-id="04a80-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="04a80-101">Get-AzWebApp</span></span>

## <span data-ttu-id="04a80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04a80-102">SYNOPSIS</span></span>
<span data-ttu-id="04a80-103">A megadott erőforráscsoport Azure Web Apps-t kap.</span><span class="sxs-lookup"><span data-stu-id="04a80-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="04a80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04a80-104">SYNTAX</span></span>

### <span data-ttu-id="04a80-105">S1</span><span class="sxs-lookup"><span data-stu-id="04a80-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04a80-106">S2</span><span class="sxs-lookup"><span data-stu-id="04a80-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04a80-107">S3</span><span class="sxs-lookup"><span data-stu-id="04a80-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04a80-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="04a80-108">DESCRIPTION</span></span>
<span data-ttu-id="04a80-109">A **Get-AzWebApp** parancsmag információkat kap az Azure Web App alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="04a80-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="04a80-110">Példák</span><span class="sxs-lookup"><span data-stu-id="04a80-110">EXAMPLES</span></span>

### <span data-ttu-id="04a80-111">Példa 1: webalkalmazás beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="04a80-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="04a80-112">Ez a parancs beilleszti a ContosoSite nevű webalkalmazást, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="04a80-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="04a80-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04a80-113">PARAMETERS</span></span>

### <span data-ttu-id="04a80-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="04a80-114">-AppServicePlan</span></span>
<span data-ttu-id="04a80-115">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="04a80-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a80-116">-DefaultProfile</span></span>
<span data-ttu-id="04a80-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04a80-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a80-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="04a80-118">-Location</span></span>
<span data-ttu-id="04a80-119">Helyre</span><span class="sxs-lookup"><span data-stu-id="04a80-119">Location</span></span>

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

### <span data-ttu-id="04a80-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04a80-120">-Name</span></span>
<span data-ttu-id="04a80-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="04a80-121">WebApp Name</span></span>

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

### <span data-ttu-id="04a80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a80-122">-ResourceGroupName</span></span>
<span data-ttu-id="04a80-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="04a80-123">Resource Group Name</span></span>

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

### <span data-ttu-id="04a80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a80-124">CommonParameters</span></span>
<span data-ttu-id="04a80-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04a80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a80-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a80-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a80-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04a80-127">INPUTS</span></span>

### <span data-ttu-id="04a80-128">System. String</span><span class="sxs-lookup"><span data-stu-id="04a80-128">System.String</span></span>

## <span data-ttu-id="04a80-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04a80-129">OUTPUTS</span></span>

### <span data-ttu-id="04a80-130">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="04a80-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="04a80-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04a80-131">NOTES</span></span>

## <span data-ttu-id="04a80-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04a80-132">RELATED LINKS</span></span>

[<span data-ttu-id="04a80-133">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="04a80-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="04a80-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="04a80-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="04a80-135">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="04a80-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="04a80-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="04a80-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="04a80-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="04a80-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


