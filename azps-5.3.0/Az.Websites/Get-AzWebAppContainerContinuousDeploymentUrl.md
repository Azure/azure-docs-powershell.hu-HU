---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380727"
---
# <span data-ttu-id="ea2ca-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="ea2ca-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="ea2ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2ca-103">Get-AzWebAppContainerContinuousDeploymentUrl tároló folyamatos telepítési URL-címét adja vissza</span><span class="sxs-lookup"><span data-stu-id="ea2ca-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="ea2ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea2ca-104">SYNTAX</span></span>

### <span data-ttu-id="ea2ca-105">S1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea2ca-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea2ca-106">S2</span><span class="sxs-lookup"><span data-stu-id="ea2ca-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea2ca-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea2ca-107">DESCRIPTION</span></span>
<span data-ttu-id="ea2ca-108">Get-AzWebAppContainerContinuousDeploymentUrl tároló folyamatos telepítési URL-címét adja vissza</span><span class="sxs-lookup"><span data-stu-id="ea2ca-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="ea2ca-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea2ca-109">EXAMPLES</span></span>

### <span data-ttu-id="ea2ca-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ea2ca-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ea2ca-111">Ez a parancs a tároló folyamatos telepítési URL-címét adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ea2ca-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="ea2ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea2ca-112">PARAMETERS</span></span>

### <span data-ttu-id="ea2ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2ca-113">-DefaultProfile</span></span>
<span data-ttu-id="ea2ca-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea2ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea2ca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ea2ca-115">-Name</span></span>
<span data-ttu-id="ea2ca-116">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="ea2ca-116">The name of the web app.</span></span>

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

### <span data-ttu-id="ea2ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea2ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea2ca-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ea2ca-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea2ca-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ea2ca-119">-SlotName</span></span>
<span data-ttu-id="ea2ca-120">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="ea2ca-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2ca-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ea2ca-121">-WebApp</span></span>
<span data-ttu-id="ea2ca-122">A webalkalmazás-objektum</span><span class="sxs-lookup"><span data-stu-id="ea2ca-122">The web app object</span></span>

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

### <span data-ttu-id="ea2ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2ca-123">CommonParameters</span></span>
<span data-ttu-id="ea2ca-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea2ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2ca-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea2ca-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2ca-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea2ca-126">INPUTS</span></span>

### <span data-ttu-id="ea2ca-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ea2ca-127">System.String</span></span>

### <span data-ttu-id="ea2ca-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ea2ca-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ea2ca-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea2ca-129">OUTPUTS</span></span>

### <span data-ttu-id="ea2ca-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ea2ca-130">System.String</span></span>

## <span data-ttu-id="ea2ca-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea2ca-131">NOTES</span></span>

## <span data-ttu-id="ea2ca-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea2ca-132">RELATED LINKS</span></span>
