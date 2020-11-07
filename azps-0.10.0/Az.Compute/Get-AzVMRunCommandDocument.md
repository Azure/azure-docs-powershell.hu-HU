---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844570"
---
# <span data-ttu-id="f9972-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="f9972-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="f9972-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9972-102">SYNOPSIS</span></span>
<span data-ttu-id="f9972-103">Futtassa a Futtatás parancsot.</span><span class="sxs-lookup"><span data-stu-id="f9972-103">Get run command document.</span></span>

## <span data-ttu-id="f9972-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9972-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9972-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9972-105">DESCRIPTION</span></span>
<span data-ttu-id="f9972-106">Futtassa a Futtatás parancsot.</span><span class="sxs-lookup"><span data-stu-id="f9972-106">Get run command document.</span></span>

## <span data-ttu-id="f9972-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f9972-107">EXAMPLES</span></span>

### <span data-ttu-id="f9972-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f9972-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="f9972-109">A ' westus ' "RunPowerShellScript" parancsára vonatkozó konkrét futtatási parancsot kap.</span><span class="sxs-lookup"><span data-stu-id="f9972-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="f9972-110">Get-AzVMRunCommandDocument-hely $loc</span><span class="sxs-lookup"><span data-stu-id="f9972-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="f9972-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="f9972-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="f9972-112">Az összes elérhető Futtatás parancs az "westus" listában.</span><span class="sxs-lookup"><span data-stu-id="f9972-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="f9972-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9972-113">PARAMETERS</span></span>

### <span data-ttu-id="f9972-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="f9972-114">-CommandId</span></span>
<span data-ttu-id="f9972-115">A parancs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f9972-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9972-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9972-116">-DefaultProfile</span></span>
<span data-ttu-id="f9972-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9972-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9972-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="f9972-118">-Location</span></span>
<span data-ttu-id="f9972-119">A futtatott parancsok lekérdezésének helye.</span><span class="sxs-lookup"><span data-stu-id="f9972-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9972-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9972-120">CommonParameters</span></span>
<span data-ttu-id="f9972-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9972-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9972-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9972-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9972-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9972-123">INPUTS</span></span>

### <span data-ttu-id="f9972-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f9972-124">System.String</span></span>

## <span data-ttu-id="f9972-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9972-125">OUTPUTS</span></span>

### <span data-ttu-id="f9972-126">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="f9972-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="f9972-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9972-127">NOTES</span></span>

## <span data-ttu-id="f9972-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9972-128">RELATED LINKS</span></span>

