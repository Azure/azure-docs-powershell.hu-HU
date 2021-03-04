---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 86d8e3bfebe8e87abacc78859dd6e776ff2ccf0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933114"
---
# <span data-ttu-id="0c5cf-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="0c5cf-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="0c5cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5cf-103">Futtatás parancsdokumentum létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c5cf-103">Get a run command document.</span></span>

## <span data-ttu-id="0c5cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c5cf-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c5cf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c5cf-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5cf-106">Futtatás parancsdokumentum létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c5cf-106">Get a run command document.</span></span>

## <span data-ttu-id="0c5cf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c5cf-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5cf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0c5cf-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="0c5cf-109">Egy adott futtatott parancsdokumentumot kap a "RunPowerShellScript" parancshoz a "westus" nyelven.</span><span class="sxs-lookup"><span data-stu-id="0c5cf-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="0c5cf-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0c5cf-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="0c5cf-111">Az összes elérhető futtatás parancs a "westus"-ban.</span><span class="sxs-lookup"><span data-stu-id="0c5cf-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="0c5cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c5cf-112">PARAMETERS</span></span>

### <span data-ttu-id="0c5cf-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="0c5cf-113">-CommandId</span></span>
<span data-ttu-id="0c5cf-114">A parancsazonosító.</span><span class="sxs-lookup"><span data-stu-id="0c5cf-114">The command ID.</span></span>

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

### <span data-ttu-id="0c5cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5cf-115">-DefaultProfile</span></span>
<span data-ttu-id="0c5cf-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c5cf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5cf-117">-Location</span><span class="sxs-lookup"><span data-stu-id="0c5cf-117">-Location</span></span>
<span data-ttu-id="0c5cf-118">A parancslekérdezés helye.</span><span class="sxs-lookup"><span data-stu-id="0c5cf-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="0c5cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5cf-119">CommonParameters</span></span>
<span data-ttu-id="0c5cf-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c5cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5cf-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c5cf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5cf-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c5cf-122">INPUTS</span></span>

### <span data-ttu-id="0c5cf-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0c5cf-123">System.String</span></span>

## <span data-ttu-id="0c5cf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c5cf-124">OUTPUTS</span></span>

### <span data-ttu-id="0c5cf-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="0c5cf-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="0c5cf-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c5cf-126">NOTES</span></span>

## <span data-ttu-id="0c5cf-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c5cf-127">RELATED LINKS</span></span>
