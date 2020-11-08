---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187969"
---
# <span data-ttu-id="73e64-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73e64-101">Start-AzWebApp</span></span>

## <span data-ttu-id="73e64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73e64-102">SYNOPSIS</span></span>
<span data-ttu-id="73e64-103">Azure Web App indítása.</span><span class="sxs-lookup"><span data-stu-id="73e64-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="73e64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73e64-104">SYNTAX</span></span>

### <span data-ttu-id="73e64-105">S1</span><span class="sxs-lookup"><span data-stu-id="73e64-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73e64-106">S2</span><span class="sxs-lookup"><span data-stu-id="73e64-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73e64-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="73e64-107">DESCRIPTION</span></span>
<span data-ttu-id="73e64-108">A **Start-AzWebApp** parancsmag az Azure web app alkalmazást indítja el.</span><span class="sxs-lookup"><span data-stu-id="73e64-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="73e64-109">Példák</span><span class="sxs-lookup"><span data-stu-id="73e64-109">EXAMPLES</span></span>

### <span data-ttu-id="73e64-110">1. példa: webalkalmazás indítása</span><span class="sxs-lookup"><span data-stu-id="73e64-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="73e64-111">Ez a parancs elindítja a ContosoWebApp nevű webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="73e64-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="73e64-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73e64-112">PARAMETERS</span></span>

### <span data-ttu-id="73e64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e64-113">-DefaultProfile</span></span>
<span data-ttu-id="73e64-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73e64-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73e64-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73e64-115">-Name</span></span>
<span data-ttu-id="73e64-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="73e64-116">WebApp Name</span></span>

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

### <span data-ttu-id="73e64-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e64-117">-ResourceGroupName</span></span>
<span data-ttu-id="73e64-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="73e64-118">Resource Group Name</span></span>

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

### <span data-ttu-id="73e64-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="73e64-119">-WebApp</span></span>
<span data-ttu-id="73e64-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="73e64-120">WebApp Object</span></span>

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

### <span data-ttu-id="73e64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e64-121">CommonParameters</span></span>
<span data-ttu-id="73e64-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73e64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e64-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e64-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e64-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73e64-124">INPUTS</span></span>

### <span data-ttu-id="73e64-125">System. String</span><span class="sxs-lookup"><span data-stu-id="73e64-125">System.String</span></span>

### <span data-ttu-id="73e64-126">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="73e64-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="73e64-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73e64-127">OUTPUTS</span></span>

### <span data-ttu-id="73e64-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="73e64-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="73e64-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73e64-129">NOTES</span></span>

## <span data-ttu-id="73e64-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73e64-130">RELATED LINKS</span></span>

[<span data-ttu-id="73e64-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73e64-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="73e64-132">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73e64-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="73e64-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73e64-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="73e64-134">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73e64-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="73e64-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73e64-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


