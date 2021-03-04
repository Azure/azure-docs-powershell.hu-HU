---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 6a3dc975c34d4938235ce95743f73f833a948b49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926041"
---
# <span data-ttu-id="3f39b-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="3f39b-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="3f39b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f39b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f39b-103">Töltse le és telepítse a metszőt, a Kubernetes parancssori eszközt.</span><span class="sxs-lookup"><span data-stu-id="3f39b-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="3f39b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f39b-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f39b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f39b-105">DESCRIPTION</span></span>
<span data-ttu-id="3f39b-106">Töltse le és telepítse a metszőt, a Kubernetes parancssori eszközt.</span><span class="sxs-lookup"><span data-stu-id="3f39b-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="3f39b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f39b-107">EXAMPLES</span></span>

### <span data-ttu-id="3f39b-108">A kutectl legújabb verziójának letöltése és telepítése</span><span class="sxs-lookup"><span data-stu-id="3f39b-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="3f39b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f39b-109">PARAMETERS</span></span>

### <span data-ttu-id="3f39b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f39b-110">-AsJob</span></span>
<span data-ttu-id="3f39b-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3f39b-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f39b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f39b-112">-DefaultProfile</span></span>
<span data-ttu-id="3f39b-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f39b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f39b-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="3f39b-114">-Destination</span></span>
<span data-ttu-id="3f39b-115">A kutectl telepítésének elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3f39b-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="3f39b-116">Alapértelmezés szerint a telepítés a ~/.azure-kutectl/</span><span class="sxs-lookup"><span data-stu-id="3f39b-116">Default to install into ~/.azure-kubectl/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f39b-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="3f39b-117">-DownloadFromMirror</span></span>
<span data-ttu-id="3f39b-118">Letöltés tükörwebhelyről: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="3f39b-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f39b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3f39b-119">-Force</span></span>
<span data-ttu-id="3f39b-120">Meglévő kutectl felülírása kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="3f39b-120">Overwrite existing kubectl without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f39b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f39b-121">-PassThru</span></span>
<span data-ttu-id="3f39b-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="3f39b-122">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f39b-123">-Version</span><span class="sxs-lookup"><span data-stu-id="3f39b-123">-Version</span></span>
<span data-ttu-id="3f39b-124">A telepítendre használt kutectl-verzió, például "v1.17.2".</span><span class="sxs-lookup"><span data-stu-id="3f39b-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="3f39b-125">Alapértelmezett érték: Legutóbbi</span><span class="sxs-lookup"><span data-stu-id="3f39b-125">Default value: Latest</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f39b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f39b-126">-Confirm</span></span>
<span data-ttu-id="3f39b-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f39b-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f39b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f39b-128">-WhatIf</span></span>
<span data-ttu-id="3f39b-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f39b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f39b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f39b-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f39b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f39b-131">CommonParameters</span></span>
<span data-ttu-id="3f39b-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f39b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f39b-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f39b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f39b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f39b-134">INPUTS</span></span>

### <span data-ttu-id="3f39b-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="3f39b-135">None</span></span>

## <span data-ttu-id="3f39b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f39b-136">OUTPUTS</span></span>

### <span data-ttu-id="3f39b-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f39b-137">System.Boolean</span></span>

## <span data-ttu-id="3f39b-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f39b-138">NOTES</span></span>

## <span data-ttu-id="3f39b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f39b-139">RELATED LINKS</span></span>
