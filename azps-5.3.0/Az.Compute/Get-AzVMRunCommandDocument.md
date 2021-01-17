---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480851"
---
# <span data-ttu-id="01f38-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="01f38-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="01f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01f38-102">SYNOPSIS</span></span>
<span data-ttu-id="01f38-103">Futtatás parancsdokumentum létrehozása</span><span class="sxs-lookup"><span data-stu-id="01f38-103">Get a run command document.</span></span>

## <span data-ttu-id="01f38-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01f38-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01f38-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01f38-105">DESCRIPTION</span></span>
<span data-ttu-id="01f38-106">Futtatás parancsdokumentum létrehozása</span><span class="sxs-lookup"><span data-stu-id="01f38-106">Get a run command document.</span></span>

## <span data-ttu-id="01f38-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01f38-107">EXAMPLES</span></span>

### <span data-ttu-id="01f38-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="01f38-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="01f38-109">Egy adott futtatott parancsdokumentumot kap a "RunPowerShellScript" parancshoz a "westus" nyelven.</span><span class="sxs-lookup"><span data-stu-id="01f38-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="01f38-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="01f38-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="01f38-111">A "westus"-ban elérhető összes futtatás parancs.</span><span class="sxs-lookup"><span data-stu-id="01f38-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="01f38-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01f38-112">PARAMETERS</span></span>

### <span data-ttu-id="01f38-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="01f38-113">-CommandId</span></span>
<span data-ttu-id="01f38-114">A parancsazonosító.</span><span class="sxs-lookup"><span data-stu-id="01f38-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f38-115">-DefaultProfile</span></span>
<span data-ttu-id="01f38-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01f38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01f38-117">-Location</span><span class="sxs-lookup"><span data-stu-id="01f38-117">-Location</span></span>
<span data-ttu-id="01f38-118">A parancslekérdezés helye.</span><span class="sxs-lookup"><span data-stu-id="01f38-118">The location upon which run commands are queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f38-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f38-119">CommonParameters</span></span>
<span data-ttu-id="01f38-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f38-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f38-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01f38-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f38-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01f38-122">INPUTS</span></span>

### <span data-ttu-id="01f38-123">System.String</span><span class="sxs-lookup"><span data-stu-id="01f38-123">System.String</span></span>

## <span data-ttu-id="01f38-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01f38-124">OUTPUTS</span></span>

### <span data-ttu-id="01f38-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="01f38-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="01f38-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01f38-126">NOTES</span></span>

## <span data-ttu-id="01f38-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01f38-127">RELATED LINKS</span></span>
