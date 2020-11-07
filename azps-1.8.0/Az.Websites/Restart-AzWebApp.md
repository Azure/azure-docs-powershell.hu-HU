---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 5b14c694ca61d5c63642012aa954b0e288551b83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668305"
---
# <span data-ttu-id="35195-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="35195-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="35195-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35195-102">SYNOPSIS</span></span>
<span data-ttu-id="35195-103">Az Azure Web App újraindítása.</span><span class="sxs-lookup"><span data-stu-id="35195-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="35195-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35195-104">SYNTAX</span></span>

### <span data-ttu-id="35195-105">S1</span><span class="sxs-lookup"><span data-stu-id="35195-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35195-106">S2</span><span class="sxs-lookup"><span data-stu-id="35195-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35195-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="35195-107">DESCRIPTION</span></span>
<span data-ttu-id="35195-108">Az **Újraindítás – AzWebApp** parancsmag leáll, majd egy Azure Web App indítása.</span><span class="sxs-lookup"><span data-stu-id="35195-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="35195-109">Ha a Web App leállított állapotban van, használja az Start-AzWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="35195-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="35195-110">Példák</span><span class="sxs-lookup"><span data-stu-id="35195-110">EXAMPLES</span></span>

### <span data-ttu-id="35195-111">1. példa: webalkalmazás újraindítása</span><span class="sxs-lookup"><span data-stu-id="35195-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="35195-112">Ez a parancs leállítja a ContosoSite nevű Azure webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport csoportjába tartozik, majd újraindul.</span><span class="sxs-lookup"><span data-stu-id="35195-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="35195-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35195-113">PARAMETERS</span></span>

### <span data-ttu-id="35195-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35195-114">-DefaultProfile</span></span>
<span data-ttu-id="35195-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35195-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35195-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35195-116">-Name</span></span>
<span data-ttu-id="35195-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="35195-117">WebApp Name</span></span>

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

### <span data-ttu-id="35195-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35195-118">-ResourceGroupName</span></span>
<span data-ttu-id="35195-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="35195-119">Resource Group Name</span></span>

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

### <span data-ttu-id="35195-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="35195-120">-WebApp</span></span>
<span data-ttu-id="35195-121">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="35195-121">WebApp Object</span></span>

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

### <span data-ttu-id="35195-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35195-122">CommonParameters</span></span>
<span data-ttu-id="35195-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35195-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35195-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35195-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35195-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35195-125">INPUTS</span></span>

### <span data-ttu-id="35195-126">System. String</span><span class="sxs-lookup"><span data-stu-id="35195-126">System.String</span></span>

### <span data-ttu-id="35195-127">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="35195-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="35195-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35195-128">OUTPUTS</span></span>

### <span data-ttu-id="35195-129">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="35195-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="35195-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35195-130">NOTES</span></span>

## <span data-ttu-id="35195-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35195-131">RELATED LINKS</span></span>

[<span data-ttu-id="35195-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="35195-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="35195-133">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="35195-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="35195-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="35195-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="35195-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="35195-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="35195-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="35195-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


