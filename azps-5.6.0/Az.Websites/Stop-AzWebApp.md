---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 102dbd678fe6fe46034a43c46cb713428b8564d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011045"
---
# <span data-ttu-id="d270f-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d270f-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="d270f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d270f-102">SYNOPSIS</span></span>
<span data-ttu-id="d270f-103">Leállítja az Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="d270f-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="d270f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d270f-104">SYNTAX</span></span>

### <span data-ttu-id="d270f-105">S1</span><span class="sxs-lookup"><span data-stu-id="d270f-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d270f-106">S2</span><span class="sxs-lookup"><span data-stu-id="d270f-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d270f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d270f-107">DESCRIPTION</span></span>
<span data-ttu-id="d270f-108">A **Stop-AzWebApp parancsmag** leállít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="d270f-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="d270f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d270f-109">EXAMPLES</span></span>

### <span data-ttu-id="d270f-110">1. példa: Webalkalmazás leállítása</span><span class="sxs-lookup"><span data-stu-id="d270f-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="d270f-111">Ez a parancs leállítja a ContosoWebApp nevű webappot, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="d270f-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d270f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d270f-112">PARAMETERS</span></span>

### <span data-ttu-id="d270f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d270f-113">-DefaultProfile</span></span>
<span data-ttu-id="d270f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d270f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d270f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d270f-115">-Name</span></span>
<span data-ttu-id="d270f-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="d270f-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d270f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d270f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d270f-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d270f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d270f-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d270f-119">-WebApp</span></span>
<span data-ttu-id="d270f-120">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="d270f-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d270f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d270f-121">CommonParameters</span></span>
<span data-ttu-id="d270f-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d270f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d270f-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d270f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d270f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d270f-124">INPUTS</span></span>

### <span data-ttu-id="d270f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d270f-125">System.String</span></span>

### <span data-ttu-id="d270f-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d270f-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d270f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d270f-127">OUTPUTS</span></span>

### <span data-ttu-id="d270f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d270f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d270f-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d270f-129">NOTES</span></span>

## <span data-ttu-id="d270f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d270f-130">RELATED LINKS</span></span>

[<span data-ttu-id="d270f-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d270f-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d270f-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d270f-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d270f-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d270f-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d270f-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d270f-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d270f-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d270f-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


