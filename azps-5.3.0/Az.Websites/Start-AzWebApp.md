---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466959"
---
# <span data-ttu-id="8fa14-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8fa14-101">Start-AzWebApp</span></span>

## <span data-ttu-id="8fa14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fa14-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa14-103">Elindít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="8fa14-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="8fa14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8fa14-104">SYNTAX</span></span>

### <span data-ttu-id="8fa14-105">S1</span><span class="sxs-lookup"><span data-stu-id="8fa14-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fa14-106">S2</span><span class="sxs-lookup"><span data-stu-id="8fa14-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fa14-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8fa14-107">DESCRIPTION</span></span>
<span data-ttu-id="8fa14-108">A **Start-AzWebApp** parancsmag elindít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="8fa14-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="8fa14-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8fa14-109">EXAMPLES</span></span>

### <span data-ttu-id="8fa14-110">1. példa: Webalkalmazás kezdése</span><span class="sxs-lookup"><span data-stu-id="8fa14-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="8fa14-111">Ez a parancs elindítja a ContosoWebApp nevű webappot, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="8fa14-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8fa14-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fa14-112">PARAMETERS</span></span>

### <span data-ttu-id="8fa14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa14-113">-DefaultProfile</span></span>
<span data-ttu-id="8fa14-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fa14-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fa14-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8fa14-115">-Name</span></span>
<span data-ttu-id="8fa14-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="8fa14-116">WebApp Name</span></span>

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

### <span data-ttu-id="8fa14-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fa14-117">-ResourceGroupName</span></span>
<span data-ttu-id="8fa14-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8fa14-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8fa14-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8fa14-119">-WebApp</span></span>
<span data-ttu-id="8fa14-120">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="8fa14-120">WebApp Object</span></span>

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

### <span data-ttu-id="8fa14-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa14-121">CommonParameters</span></span>
<span data-ttu-id="8fa14-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa14-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa14-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa14-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa14-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fa14-124">INPUTS</span></span>

### <span data-ttu-id="8fa14-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8fa14-125">System.String</span></span>

### <span data-ttu-id="8fa14-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8fa14-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8fa14-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fa14-127">OUTPUTS</span></span>

### <span data-ttu-id="8fa14-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8fa14-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8fa14-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8fa14-129">NOTES</span></span>

## <span data-ttu-id="8fa14-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fa14-130">RELATED LINKS</span></span>

[<span data-ttu-id="8fa14-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8fa14-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="8fa14-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8fa14-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8fa14-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8fa14-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8fa14-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8fa14-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="8fa14-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8fa14-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


