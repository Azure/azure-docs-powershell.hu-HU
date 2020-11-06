---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 034736bf55eb6dc13f7ba8a51ec57da728733eb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492658"
---
# <span data-ttu-id="6b0ff-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6b0ff-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="6b0ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="6b0ff-103">Azure Web App indítása.</span><span class="sxs-lookup"><span data-stu-id="6b0ff-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b0ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b0ff-104">SYNTAX</span></span>

### <span data-ttu-id="6b0ff-105">S1</span><span class="sxs-lookup"><span data-stu-id="6b0ff-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b0ff-106">S2</span><span class="sxs-lookup"><span data-stu-id="6b0ff-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b0ff-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b0ff-107">DESCRIPTION</span></span>
<span data-ttu-id="6b0ff-108">A **Start-AzureRmWebApp** parancsmag az Azure web app alkalmazást indítja el.</span><span class="sxs-lookup"><span data-stu-id="6b0ff-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="6b0ff-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6b0ff-109">EXAMPLES</span></span>

### <span data-ttu-id="6b0ff-110">1. példa: webalkalmazás indítása</span><span class="sxs-lookup"><span data-stu-id="6b0ff-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="6b0ff-111">Ez a parancs elindítja a ContosoWebApp nevű webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b0ff-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6b0ff-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b0ff-112">PARAMETERS</span></span>

### <span data-ttu-id="6b0ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b0ff-113">-DefaultProfile</span></span>
<span data-ttu-id="6b0ff-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b0ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b0ff-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b0ff-115">-Name</span></span>
<span data-ttu-id="6b0ff-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="6b0ff-116">WebApp Name</span></span>

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

### <span data-ttu-id="6b0ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b0ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="6b0ff-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="6b0ff-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6b0ff-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6b0ff-119">-WebApp</span></span>
<span data-ttu-id="6b0ff-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="6b0ff-120">WebApp Object</span></span>

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

### <span data-ttu-id="6b0ff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b0ff-121">CommonParameters</span></span>
<span data-ttu-id="6b0ff-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b0ff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b0ff-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b0ff-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b0ff-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b0ff-124">INPUTS</span></span>

### <span data-ttu-id="6b0ff-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6b0ff-125">System.String</span></span>

### <span data-ttu-id="6b0ff-126">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="6b0ff-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6b0ff-127">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b0ff-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6b0ff-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b0ff-128">OUTPUTS</span></span>

### <span data-ttu-id="6b0ff-129">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="6b0ff-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="6b0ff-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b0ff-130">NOTES</span></span>

## <span data-ttu-id="6b0ff-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b0ff-131">RELATED LINKS</span></span>

[<span data-ttu-id="6b0ff-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6b0ff-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="6b0ff-133">Új – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6b0ff-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="6b0ff-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6b0ff-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="6b0ff-135">Újraindítás – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6b0ff-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="6b0ff-136">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6b0ff-136">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


