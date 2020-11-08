---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195638"
---
# <span data-ttu-id="0cb03-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb03-101">Get-AzWebApp</span></span>

## <span data-ttu-id="0cb03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cb03-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb03-103">A megadott erőforráscsoport Azure Web Apps-t kap.</span><span class="sxs-lookup"><span data-stu-id="0cb03-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="0cb03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cb03-104">SYNTAX</span></span>

### <span data-ttu-id="0cb03-105">S1</span><span class="sxs-lookup"><span data-stu-id="0cb03-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0cb03-106">S2</span><span class="sxs-lookup"><span data-stu-id="0cb03-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0cb03-107">S3</span><span class="sxs-lookup"><span data-stu-id="0cb03-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cb03-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cb03-108">DESCRIPTION</span></span>
<span data-ttu-id="0cb03-109">A **Get-AzWebApp** parancsmag információkat kap az Azure Web App alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="0cb03-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="0cb03-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0cb03-110">EXAMPLES</span></span>

### <span data-ttu-id="0cb03-111">Példa 1: webalkalmazás beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="0cb03-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="0cb03-112">Ez a parancs beilleszti a ContosoSite nevű webalkalmazást, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="0cb03-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0cb03-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cb03-113">PARAMETERS</span></span>

### <span data-ttu-id="0cb03-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0cb03-114">-AppServicePlan</span></span>
<span data-ttu-id="0cb03-115">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="0cb03-115">App Service Plan object</span></span>

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

### <span data-ttu-id="0cb03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb03-116">-DefaultProfile</span></span>
<span data-ttu-id="0cb03-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cb03-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cb03-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="0cb03-118">-Location</span></span>
<span data-ttu-id="0cb03-119">Helyre</span><span class="sxs-lookup"><span data-stu-id="0cb03-119">Location</span></span>

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

### <span data-ttu-id="0cb03-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0cb03-120">-Name</span></span>
<span data-ttu-id="0cb03-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="0cb03-121">WebApp Name</span></span>

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

### <span data-ttu-id="0cb03-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cb03-122">-ResourceGroupName</span></span>
<span data-ttu-id="0cb03-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0cb03-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0cb03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb03-124">CommonParameters</span></span>
<span data-ttu-id="0cb03-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cb03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb03-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cb03-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb03-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cb03-127">INPUTS</span></span>

### <span data-ttu-id="0cb03-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0cb03-128">System.String</span></span>

## <span data-ttu-id="0cb03-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cb03-129">OUTPUTS</span></span>

### <span data-ttu-id="0cb03-130">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0cb03-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0cb03-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cb03-131">NOTES</span></span>

## <span data-ttu-id="0cb03-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cb03-132">RELATED LINKS</span></span>

[<span data-ttu-id="0cb03-133">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb03-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0cb03-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb03-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0cb03-135">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb03-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0cb03-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb03-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0cb03-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb03-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

