---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012585"
---
# <span data-ttu-id="20249-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20249-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="20249-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20249-102">SYNOPSIS</span></span>
<span data-ttu-id="20249-103">Azure Web App leállítása</span><span class="sxs-lookup"><span data-stu-id="20249-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="20249-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20249-104">SYNTAX</span></span>

### <span data-ttu-id="20249-105">S1</span><span class="sxs-lookup"><span data-stu-id="20249-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20249-106">S2</span><span class="sxs-lookup"><span data-stu-id="20249-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20249-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="20249-107">DESCRIPTION</span></span>
<span data-ttu-id="20249-108">A **stop-AzWebApp** parancsmag leállítja az Azure web app alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="20249-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="20249-109">Példák</span><span class="sxs-lookup"><span data-stu-id="20249-109">EXAMPLES</span></span>

### <span data-ttu-id="20249-110">Példa 1: webalkalmazás leállítása</span><span class="sxs-lookup"><span data-stu-id="20249-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="20249-111">Ez a parancs leállítja a ContosoWebApp nevű webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="20249-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="20249-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20249-112">PARAMETERS</span></span>

### <span data-ttu-id="20249-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20249-113">-DefaultProfile</span></span>
<span data-ttu-id="20249-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20249-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20249-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20249-115">-Name</span></span>
<span data-ttu-id="20249-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="20249-116">WebApp Name</span></span>

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

### <span data-ttu-id="20249-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20249-117">-ResourceGroupName</span></span>
<span data-ttu-id="20249-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="20249-118">Resource Group Name</span></span>

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

### <span data-ttu-id="20249-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="20249-119">-WebApp</span></span>
<span data-ttu-id="20249-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="20249-120">WebApp Object</span></span>

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

### <span data-ttu-id="20249-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20249-121">CommonParameters</span></span>
<span data-ttu-id="20249-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20249-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20249-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20249-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20249-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20249-124">INPUTS</span></span>

### <span data-ttu-id="20249-125">System. String</span><span class="sxs-lookup"><span data-stu-id="20249-125">System.String</span></span>

### <span data-ttu-id="20249-126">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="20249-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="20249-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20249-127">OUTPUTS</span></span>

### <span data-ttu-id="20249-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="20249-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="20249-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20249-129">NOTES</span></span>

## <span data-ttu-id="20249-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20249-130">RELATED LINKS</span></span>

[<span data-ttu-id="20249-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20249-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="20249-132">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20249-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="20249-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20249-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="20249-134">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20249-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="20249-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20249-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


