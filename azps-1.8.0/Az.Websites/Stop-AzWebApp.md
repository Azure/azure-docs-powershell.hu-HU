---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 28a6399db8f896d60c48d62d69ca75c5d85c25c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668285"
---
# <span data-ttu-id="a3a5a-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a5a-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="a3a5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a5a-103">Azure Web App leállítása</span><span class="sxs-lookup"><span data-stu-id="a3a5a-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="a3a5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3a5a-104">SYNTAX</span></span>

### <span data-ttu-id="a3a5a-105">S1</span><span class="sxs-lookup"><span data-stu-id="a3a5a-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3a5a-106">S2</span><span class="sxs-lookup"><span data-stu-id="a3a5a-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3a5a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3a5a-107">DESCRIPTION</span></span>
<span data-ttu-id="a3a5a-108">A **stop-AzWebApp** parancsmag leállítja az Azure web app alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="a3a5a-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="a3a5a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a3a5a-109">EXAMPLES</span></span>

### <span data-ttu-id="a3a5a-110">Példa 1: webalkalmazás leállítása</span><span class="sxs-lookup"><span data-stu-id="a3a5a-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a3a5a-111">Ez a parancs leállítja a ContosoWebApp nevű webalkalmazást, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="a3a5a-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a3a5a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3a5a-112">PARAMETERS</span></span>

### <span data-ttu-id="a3a5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a5a-113">-DefaultProfile</span></span>
<span data-ttu-id="a3a5a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3a5a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3a5a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3a5a-115">-Name</span></span>
<span data-ttu-id="a3a5a-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="a3a5a-116">WebApp Name</span></span>

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

### <span data-ttu-id="a3a5a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a5a-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3a5a-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a3a5a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a3a5a-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a3a5a-119">-WebApp</span></span>
<span data-ttu-id="a3a5a-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="a3a5a-120">WebApp Object</span></span>

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

### <span data-ttu-id="a3a5a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a5a-121">CommonParameters</span></span>
<span data-ttu-id="a3a5a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3a5a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a5a-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a5a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a5a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3a5a-124">INPUTS</span></span>

### <span data-ttu-id="a3a5a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a3a5a-125">System.String</span></span>

### <span data-ttu-id="a3a5a-126">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a3a5a-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a3a5a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3a5a-127">OUTPUTS</span></span>

### <span data-ttu-id="a3a5a-128">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a3a5a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a3a5a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3a5a-129">NOTES</span></span>

## <span data-ttu-id="a3a5a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3a5a-130">RELATED LINKS</span></span>

[<span data-ttu-id="a3a5a-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a5a-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a3a5a-132">Új – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a5a-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a3a5a-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a5a-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a3a5a-134">Újraindítás – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a5a-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a3a5a-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a5a-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


