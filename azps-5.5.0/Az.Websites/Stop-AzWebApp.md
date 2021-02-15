---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164434"
---
# <span data-ttu-id="0588c-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0588c-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="0588c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0588c-102">SYNOPSIS</span></span>
<span data-ttu-id="0588c-103">Leállítja az Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="0588c-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="0588c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0588c-104">SYNTAX</span></span>

### <span data-ttu-id="0588c-105">S1</span><span class="sxs-lookup"><span data-stu-id="0588c-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0588c-106">S2</span><span class="sxs-lookup"><span data-stu-id="0588c-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0588c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0588c-107">DESCRIPTION</span></span>
<span data-ttu-id="0588c-108">A **Stop-AzWebApp parancsmag** leállít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="0588c-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="0588c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0588c-109">EXAMPLES</span></span>

### <span data-ttu-id="0588c-110">1. példa: Webalkalmazás leállítása</span><span class="sxs-lookup"><span data-stu-id="0588c-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="0588c-111">Ez a parancs leállítja a ContosoWebApp nevű webappot, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="0588c-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0588c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0588c-112">PARAMETERS</span></span>

### <span data-ttu-id="0588c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0588c-113">-DefaultProfile</span></span>
<span data-ttu-id="0588c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0588c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0588c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0588c-115">-Name</span></span>
<span data-ttu-id="0588c-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="0588c-116">WebApp Name</span></span>

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

### <span data-ttu-id="0588c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0588c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0588c-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0588c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0588c-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0588c-119">-WebApp</span></span>
<span data-ttu-id="0588c-120">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="0588c-120">WebApp Object</span></span>

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

### <span data-ttu-id="0588c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0588c-121">CommonParameters</span></span>
<span data-ttu-id="0588c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0588c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0588c-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0588c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0588c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0588c-124">INPUTS</span></span>

### <span data-ttu-id="0588c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0588c-125">System.String</span></span>

### <span data-ttu-id="0588c-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0588c-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0588c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0588c-127">OUTPUTS</span></span>

### <span data-ttu-id="0588c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0588c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0588c-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0588c-129">NOTES</span></span>

## <span data-ttu-id="0588c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0588c-130">RELATED LINKS</span></span>

[<span data-ttu-id="0588c-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0588c-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0588c-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0588c-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0588c-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0588c-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0588c-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0588c-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0588c-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0588c-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


