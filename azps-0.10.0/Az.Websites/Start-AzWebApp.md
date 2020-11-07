---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: d533a2d7401236e374ca6f541e646cb85a080f9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842670"
---
# <span data-ttu-id="c279a-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c279a-101">Start-AzWebApp</span></span>

## <span data-ttu-id="c279a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c279a-102">SYNOPSIS</span></span>
<span data-ttu-id="c279a-103">Azure Web App indítása.</span><span class="sxs-lookup"><span data-stu-id="c279a-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="c279a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c279a-104">SYNTAX</span></span>

### <span data-ttu-id="c279a-105">S1</span><span class="sxs-lookup"><span data-stu-id="c279a-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c279a-106">S2</span><span class="sxs-lookup"><span data-stu-id="c279a-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c279a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c279a-107">DESCRIPTION</span></span>
<span data-ttu-id="c279a-108">A **Start-AzWebApp** parancsmag az Azure web app alkalmazást indítja el.</span><span class="sxs-lookup"><span data-stu-id="c279a-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="c279a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c279a-109">EXAMPLES</span></span>

### <span data-ttu-id="c279a-110">1. példa: webalkalmazás indítása</span><span class="sxs-lookup"><span data-stu-id="c279a-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c279a-111">Ez a parancs elindítja a ContosoWebApp nevű webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="c279a-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c279a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c279a-112">PARAMETERS</span></span>

### <span data-ttu-id="c279a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c279a-113">-DefaultProfile</span></span>
<span data-ttu-id="c279a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c279a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c279a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c279a-115">-Name</span></span>
<span data-ttu-id="c279a-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c279a-116">WebApp Name</span></span>

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

### <span data-ttu-id="c279a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c279a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c279a-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c279a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c279a-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c279a-119">-WebApp</span></span>
<span data-ttu-id="c279a-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c279a-120">WebApp Object</span></span>

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

### <span data-ttu-id="c279a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c279a-121">CommonParameters</span></span>
<span data-ttu-id="c279a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c279a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c279a-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c279a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c279a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c279a-124">INPUTS</span></span>

### <span data-ttu-id="c279a-125">Webhely</span><span class="sxs-lookup"><span data-stu-id="c279a-125">Site</span></span>
<span data-ttu-id="c279a-126">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c279a-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c279a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c279a-127">OUTPUTS</span></span>

## <span data-ttu-id="c279a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c279a-128">NOTES</span></span>

## <span data-ttu-id="c279a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c279a-129">RELATED LINKS</span></span>

[<span data-ttu-id="c279a-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c279a-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c279a-131">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c279a-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c279a-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c279a-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c279a-133">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c279a-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c279a-134">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c279a-134">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


