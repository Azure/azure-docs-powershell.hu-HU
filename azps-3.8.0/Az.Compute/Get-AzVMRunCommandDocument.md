---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012966"
---
# <span data-ttu-id="dd16d-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="dd16d-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="dd16d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd16d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd16d-103">Futtathatja a Futtatás parancs dokumentumát.</span><span class="sxs-lookup"><span data-stu-id="dd16d-103">Get a run command document.</span></span>

## <span data-ttu-id="dd16d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd16d-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd16d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd16d-105">DESCRIPTION</span></span>
<span data-ttu-id="dd16d-106">Futtathatja a Futtatás parancs dokumentumát.</span><span class="sxs-lookup"><span data-stu-id="dd16d-106">Get a run command document.</span></span>

## <span data-ttu-id="dd16d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dd16d-107">EXAMPLES</span></span>

### <span data-ttu-id="dd16d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd16d-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="dd16d-109">A ' westus ' "RunPowerShellScript" parancsára vonatkozó konkrét futtatási parancsot kap.</span><span class="sxs-lookup"><span data-stu-id="dd16d-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="dd16d-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="dd16d-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="dd16d-111">Az összes elérhető Futtatás parancs az "westus" listában.</span><span class="sxs-lookup"><span data-stu-id="dd16d-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="dd16d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd16d-112">PARAMETERS</span></span>

### <span data-ttu-id="dd16d-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="dd16d-113">-CommandId</span></span>
<span data-ttu-id="dd16d-114">A parancs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd16d-114">The command ID.</span></span>

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

### <span data-ttu-id="dd16d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd16d-115">-DefaultProfile</span></span>
<span data-ttu-id="dd16d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd16d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd16d-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="dd16d-117">-Location</span></span>
<span data-ttu-id="dd16d-118">A futtatott parancsok lekérdezésének helye.</span><span class="sxs-lookup"><span data-stu-id="dd16d-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="dd16d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd16d-119">CommonParameters</span></span>
<span data-ttu-id="dd16d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd16d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd16d-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dd16d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd16d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd16d-122">INPUTS</span></span>

### <span data-ttu-id="dd16d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dd16d-123">System.String</span></span>

## <span data-ttu-id="dd16d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd16d-124">OUTPUTS</span></span>

### <span data-ttu-id="dd16d-125">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="dd16d-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="dd16d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd16d-126">NOTES</span></span>

## <span data-ttu-id="dd16d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd16d-127">RELATED LINKS</span></span>
