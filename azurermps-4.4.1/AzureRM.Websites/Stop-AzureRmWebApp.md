---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: 6591250c903b3f51ccbbd567e290f9d83fab983a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492436"
---
# <span data-ttu-id="50e0a-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="50e0a-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="50e0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="50e0a-103">Azure Web App leállítása</span><span class="sxs-lookup"><span data-stu-id="50e0a-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50e0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50e0a-104">SYNTAX</span></span>

### <span data-ttu-id="50e0a-105">S1</span><span class="sxs-lookup"><span data-stu-id="50e0a-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50e0a-106">S2</span><span class="sxs-lookup"><span data-stu-id="50e0a-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50e0a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="50e0a-107">DESCRIPTION</span></span>
<span data-ttu-id="50e0a-108">A **stop-AzureRmWebApp** parancsmag leállítja az Azure web app alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="50e0a-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="50e0a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="50e0a-109">EXAMPLES</span></span>

### <span data-ttu-id="50e0a-110">Példa 1: webalkalmazás leállítása</span><span class="sxs-lookup"><span data-stu-id="50e0a-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="50e0a-111">Ez a parancs leállítja a ContosoWebApp nevű webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="50e0a-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="50e0a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50e0a-112">PARAMETERS</span></span>

### <span data-ttu-id="50e0a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="50e0a-113">-Name</span></span>
<span data-ttu-id="50e0a-114">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="50e0a-114">WebApp Name</span></span>

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

### <span data-ttu-id="50e0a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e0a-115">-ResourceGroupName</span></span>
<span data-ttu-id="50e0a-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="50e0a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="50e0a-117">-WebApp</span><span class="sxs-lookup"><span data-stu-id="50e0a-117">-WebApp</span></span>
<span data-ttu-id="50e0a-118">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="50e0a-118">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50e0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e0a-119">-DefaultProfile</span></span>
<span data-ttu-id="50e0a-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50e0a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50e0a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e0a-121">CommonParameters</span></span>
<span data-ttu-id="50e0a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50e0a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e0a-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e0a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e0a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50e0a-124">INPUTS</span></span>

### <span data-ttu-id="50e0a-125">Webhely</span><span class="sxs-lookup"><span data-stu-id="50e0a-125">Site</span></span>
<span data-ttu-id="50e0a-126">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="50e0a-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="50e0a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50e0a-127">OUTPUTS</span></span>

## <span data-ttu-id="50e0a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50e0a-128">NOTES</span></span>

## <span data-ttu-id="50e0a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50e0a-129">RELATED LINKS</span></span>

[<span data-ttu-id="50e0a-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="50e0a-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="50e0a-131">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="50e0a-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="50e0a-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="50e0a-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="50e0a-133">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="50e0a-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="50e0a-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="50e0a-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


