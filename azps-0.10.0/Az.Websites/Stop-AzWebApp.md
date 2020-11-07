---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842642"
---
# <span data-ttu-id="e0dbe-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e0dbe-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="e0dbe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dbe-103">Azure Web App leállítása</span><span class="sxs-lookup"><span data-stu-id="e0dbe-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="e0dbe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0dbe-104">SYNTAX</span></span>

### <span data-ttu-id="e0dbe-105">S1</span><span class="sxs-lookup"><span data-stu-id="e0dbe-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0dbe-106">S2</span><span class="sxs-lookup"><span data-stu-id="e0dbe-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0dbe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0dbe-107">DESCRIPTION</span></span>
<span data-ttu-id="e0dbe-108">A **stop-AzWebApp** parancsmag leállítja az Azure web app alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="e0dbe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e0dbe-109">EXAMPLES</span></span>

### <span data-ttu-id="e0dbe-110">Példa 1: webalkalmazás leállítása</span><span class="sxs-lookup"><span data-stu-id="e0dbe-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="e0dbe-111">Ez a parancs leállítja a ContosoWebApp nevű webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e0dbe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0dbe-112">PARAMETERS</span></span>

### <span data-ttu-id="e0dbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dbe-113">-DefaultProfile</span></span>
<span data-ttu-id="e0dbe-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0dbe-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0dbe-115">-Name</span></span>
<span data-ttu-id="e0dbe-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e0dbe-116">WebApp Name</span></span>

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

### <span data-ttu-id="e0dbe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0dbe-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0dbe-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e0dbe-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e0dbe-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e0dbe-119">-WebApp</span></span>
<span data-ttu-id="e0dbe-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="e0dbe-120">WebApp Object</span></span>

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

### <span data-ttu-id="e0dbe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dbe-121">CommonParameters</span></span>
<span data-ttu-id="e0dbe-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0dbe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dbe-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dbe-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0dbe-124">INPUTS</span></span>

### <span data-ttu-id="e0dbe-125">Webhely</span><span class="sxs-lookup"><span data-stu-id="e0dbe-125">Site</span></span>
<span data-ttu-id="e0dbe-126">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e0dbe-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e0dbe-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0dbe-127">OUTPUTS</span></span>

## <span data-ttu-id="e0dbe-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0dbe-128">NOTES</span></span>

## <span data-ttu-id="e0dbe-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0dbe-129">RELATED LINKS</span></span>

[<span data-ttu-id="e0dbe-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e0dbe-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e0dbe-131">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e0dbe-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e0dbe-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e0dbe-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e0dbe-133">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e0dbe-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e0dbe-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e0dbe-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


