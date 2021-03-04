---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 32e71b33b3c440701e501c4b68d740dcf121001d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934554"
---
# <span data-ttu-id="95cd3-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="95cd3-101">Get-AzWebApp</span></span>

## <span data-ttu-id="95cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="95cd3-103">Az Azure Web Apps alkalmazást a megadott erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="95cd3-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="95cd3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95cd3-104">SYNTAX</span></span>

### <span data-ttu-id="95cd3-105">S1</span><span class="sxs-lookup"><span data-stu-id="95cd3-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95cd3-106">S2</span><span class="sxs-lookup"><span data-stu-id="95cd3-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95cd3-107">S3</span><span class="sxs-lookup"><span data-stu-id="95cd3-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95cd3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95cd3-108">DESCRIPTION</span></span>
<span data-ttu-id="95cd3-109">A **Get-AzWebApp** parancsmag információkat kap az Azure Web Appról.</span><span class="sxs-lookup"><span data-stu-id="95cd3-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="95cd3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95cd3-110">EXAMPLES</span></span>

### <span data-ttu-id="95cd3-111">1. példa: Webalkalmazás lekérte egy erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="95cd3-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="95cd3-112">Ez a parancs a ContosoSite nevű webalkalmazást kapja meg, amely a Default-Web-WestUS erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="95cd3-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="95cd3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95cd3-113">PARAMETERS</span></span>

### <span data-ttu-id="95cd3-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95cd3-114">-AppServicePlan</span></span>
<span data-ttu-id="95cd3-115">App Service Plan objektum</span><span class="sxs-lookup"><span data-stu-id="95cd3-115">App Service Plan object</span></span>

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

### <span data-ttu-id="95cd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95cd3-116">-DefaultProfile</span></span>
<span data-ttu-id="95cd3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95cd3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95cd3-118">-Location</span><span class="sxs-lookup"><span data-stu-id="95cd3-118">-Location</span></span>
<span data-ttu-id="95cd3-119">Hely</span><span class="sxs-lookup"><span data-stu-id="95cd3-119">Location</span></span>

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

### <span data-ttu-id="95cd3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="95cd3-120">-Name</span></span>
<span data-ttu-id="95cd3-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="95cd3-121">WebApp Name</span></span>

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

### <span data-ttu-id="95cd3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95cd3-122">-ResourceGroupName</span></span>
<span data-ttu-id="95cd3-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="95cd3-123">Resource Group Name</span></span>

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

### <span data-ttu-id="95cd3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95cd3-124">CommonParameters</span></span>
<span data-ttu-id="95cd3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95cd3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95cd3-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95cd3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95cd3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95cd3-127">INPUTS</span></span>

### <span data-ttu-id="95cd3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="95cd3-128">System.String</span></span>

## <span data-ttu-id="95cd3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95cd3-129">OUTPUTS</span></span>

### <span data-ttu-id="95cd3-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="95cd3-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="95cd3-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95cd3-131">NOTES</span></span>

## <span data-ttu-id="95cd3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95cd3-132">RELATED LINKS</span></span>

[<span data-ttu-id="95cd3-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="95cd3-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="95cd3-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="95cd3-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="95cd3-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="95cd3-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="95cd3-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="95cd3-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="95cd3-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="95cd3-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


