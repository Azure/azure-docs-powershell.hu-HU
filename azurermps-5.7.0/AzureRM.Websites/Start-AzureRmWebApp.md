---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 74f0fcfdcbbc71781debef62becb36018ecb51a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492111"
---
# <span data-ttu-id="f2e7d-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2e7d-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="f2e7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e7d-103">Azure Web App indítása.</span><span class="sxs-lookup"><span data-stu-id="f2e7d-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2e7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2e7d-104">SYNTAX</span></span>

### <span data-ttu-id="f2e7d-105">S1</span><span class="sxs-lookup"><span data-stu-id="f2e7d-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2e7d-106">S2</span><span class="sxs-lookup"><span data-stu-id="f2e7d-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2e7d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2e7d-107">DESCRIPTION</span></span>
<span data-ttu-id="f2e7d-108">A **Start-AzureRmWebApp** parancsmag az Azure web app alkalmazást indítja el.</span><span class="sxs-lookup"><span data-stu-id="f2e7d-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="f2e7d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2e7d-109">EXAMPLES</span></span>

### <span data-ttu-id="f2e7d-110">1. példa: webalkalmazás indítása</span><span class="sxs-lookup"><span data-stu-id="f2e7d-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="f2e7d-111">Ez a parancs elindítja a ContosoWebApp nevű webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="f2e7d-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f2e7d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2e7d-112">PARAMETERS</span></span>

### <span data-ttu-id="f2e7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e7d-113">-DefaultProfile</span></span>
<span data-ttu-id="f2e7d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2e7d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e7d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2e7d-115">-Name</span></span>
<span data-ttu-id="f2e7d-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f2e7d-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2e7d-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f2e7d-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e7d-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f2e7d-119">-WebApp</span></span>
<span data-ttu-id="f2e7d-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="f2e7d-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e7d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e7d-121">CommonParameters</span></span>
<span data-ttu-id="f2e7d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2e7d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e7d-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e7d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e7d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2e7d-124">INPUTS</span></span>

### <span data-ttu-id="f2e7d-125">Webhely</span><span class="sxs-lookup"><span data-stu-id="f2e7d-125">Site</span></span>
<span data-ttu-id="f2e7d-126">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f2e7d-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f2e7d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2e7d-127">OUTPUTS</span></span>

## <span data-ttu-id="f2e7d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2e7d-128">NOTES</span></span>

## <span data-ttu-id="f2e7d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2e7d-129">RELATED LINKS</span></span>

[<span data-ttu-id="f2e7d-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2e7d-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f2e7d-131">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2e7d-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f2e7d-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2e7d-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="f2e7d-133">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2e7d-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f2e7d-134">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2e7d-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


