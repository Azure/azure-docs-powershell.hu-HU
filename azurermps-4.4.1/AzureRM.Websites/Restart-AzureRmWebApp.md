---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: eb75a4fa0ebeb121cd39e591b8cb8d46909deb42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492443"
---
# <span data-ttu-id="4cea0-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4cea0-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="4cea0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4cea0-102">SYNOPSIS</span></span>
<span data-ttu-id="4cea0-103">Az Azure Web App újraindítása.</span><span class="sxs-lookup"><span data-stu-id="4cea0-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cea0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4cea0-104">SYNTAX</span></span>

### <span data-ttu-id="4cea0-105">S1</span><span class="sxs-lookup"><span data-stu-id="4cea0-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cea0-106">S2</span><span class="sxs-lookup"><span data-stu-id="4cea0-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cea0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4cea0-107">DESCRIPTION</span></span>
<span data-ttu-id="4cea0-108">Az **Újraindítás – AzureRmWebApp** parancsmag leáll, majd egy Azure Web App indítása.</span><span class="sxs-lookup"><span data-stu-id="4cea0-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="4cea0-109">Ha a Web App leállított állapotban van, használja az Start-AzureRmWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4cea0-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="4cea0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4cea0-110">EXAMPLES</span></span>

### <span data-ttu-id="4cea0-111">1. példa: webalkalmazás újraindítása</span><span class="sxs-lookup"><span data-stu-id="4cea0-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="4cea0-112">Ez a parancs leállítja a ContosoSite nevű Azure webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport csoportjába tartozik, majd újraindul.</span><span class="sxs-lookup"><span data-stu-id="4cea0-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="4cea0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4cea0-113">PARAMETERS</span></span>

### <span data-ttu-id="4cea0-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4cea0-114">-Name</span></span>
<span data-ttu-id="4cea0-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="4cea0-115">WebApp Name</span></span>

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

### <span data-ttu-id="4cea0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cea0-116">-ResourceGroupName</span></span>
<span data-ttu-id="4cea0-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4cea0-117">Resource Group Name</span></span>

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

### <span data-ttu-id="4cea0-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4cea0-118">-WebApp</span></span>
<span data-ttu-id="4cea0-119">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="4cea0-119">WebApp Object</span></span>

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

### <span data-ttu-id="4cea0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cea0-120">-DefaultProfile</span></span>
<span data-ttu-id="4cea0-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4cea0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cea0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cea0-122">CommonParameters</span></span>
<span data-ttu-id="4cea0-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4cea0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cea0-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cea0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cea0-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cea0-125">INPUTS</span></span>

### <span data-ttu-id="4cea0-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="4cea0-126">Site</span></span>
<span data-ttu-id="4cea0-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4cea0-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4cea0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cea0-128">OUTPUTS</span></span>

## <span data-ttu-id="4cea0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4cea0-129">NOTES</span></span>

## <span data-ttu-id="4cea0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4cea0-130">RELATED LINKS</span></span>

[<span data-ttu-id="4cea0-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4cea0-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="4cea0-132">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4cea0-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="4cea0-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4cea0-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="4cea0-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4cea0-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="4cea0-135">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4cea0-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


