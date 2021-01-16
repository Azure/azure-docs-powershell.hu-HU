---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326042"
---
# <span data-ttu-id="b5802-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b5802-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="b5802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5802-102">SYNOPSIS</span></span>
<span data-ttu-id="b5802-103">Egy Azure Web App újraindítása.</span><span class="sxs-lookup"><span data-stu-id="b5802-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="b5802-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5802-104">SYNTAX</span></span>

### <span data-ttu-id="b5802-105">S1</span><span class="sxs-lookup"><span data-stu-id="b5802-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5802-106">S2</span><span class="sxs-lookup"><span data-stu-id="b5802-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5802-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5802-107">DESCRIPTION</span></span>
<span data-ttu-id="b5802-108">Az **Restart-AzWebApp** parancsmag leáll, majd elindít egy Azure Web Appot.</span><span class="sxs-lookup"><span data-stu-id="b5802-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="b5802-109">Ha a Web App leállt állapotban van, használja a Start-AzWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b5802-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="b5802-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5802-110">EXAMPLES</span></span>

### <span data-ttu-id="b5802-111">1. példa: Webalkalmazás újraindítása</span><span class="sxs-lookup"><span data-stu-id="b5802-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b5802-112">Ez a parancs leállítja a ContosoSite nevű Azure Web Appot, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik, majd újraindítja.</span><span class="sxs-lookup"><span data-stu-id="b5802-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="b5802-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5802-113">PARAMETERS</span></span>

### <span data-ttu-id="b5802-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5802-114">-DefaultProfile</span></span>
<span data-ttu-id="b5802-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5802-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5802-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b5802-116">-Name</span></span>
<span data-ttu-id="b5802-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="b5802-117">WebApp Name</span></span>

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

### <span data-ttu-id="b5802-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5802-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5802-119">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b5802-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b5802-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b5802-120">-WebApp</span></span>
<span data-ttu-id="b5802-121">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="b5802-121">WebApp Object</span></span>

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

### <span data-ttu-id="b5802-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5802-122">CommonParameters</span></span>
<span data-ttu-id="b5802-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5802-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5802-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5802-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5802-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5802-125">INPUTS</span></span>

### <span data-ttu-id="b5802-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b5802-126">System.String</span></span>

### <span data-ttu-id="b5802-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b5802-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b5802-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5802-128">OUTPUTS</span></span>

### <span data-ttu-id="b5802-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b5802-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b5802-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5802-130">NOTES</span></span>

## <span data-ttu-id="b5802-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5802-131">RELATED LINKS</span></span>

[<span data-ttu-id="b5802-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b5802-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b5802-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b5802-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b5802-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b5802-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="b5802-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b5802-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b5802-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b5802-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


