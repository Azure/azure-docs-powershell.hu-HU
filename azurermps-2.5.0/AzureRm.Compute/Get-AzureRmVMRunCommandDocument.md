---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
ms.openlocfilehash: d51528cab51e4e6fe6cda428e25965d65c449c4b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850146"
---
# <span data-ttu-id="1df85-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="1df85-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="1df85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1df85-102">SYNOPSIS</span></span>
<span data-ttu-id="1df85-103">Futtassa a Futtatás parancsot.</span><span class="sxs-lookup"><span data-stu-id="1df85-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1df85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1df85-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1df85-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1df85-105">DESCRIPTION</span></span>
<span data-ttu-id="1df85-106">Futtassa a Futtatás parancsot.</span><span class="sxs-lookup"><span data-stu-id="1df85-106">Get run command document.</span></span>

## <span data-ttu-id="1df85-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1df85-107">EXAMPLES</span></span>

### <span data-ttu-id="1df85-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1df85-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="1df85-109">A ' westus ' "RunPowerShellScript" parancsára vonatkozó konkrét futtatási parancsot kap.</span><span class="sxs-lookup"><span data-stu-id="1df85-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="1df85-110">Get-AzureRmVMRunCommandDocument-hely $loc</span><span class="sxs-lookup"><span data-stu-id="1df85-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="1df85-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="1df85-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="1df85-112">Az összes elérhető Futtatás parancs az "westus" listában.</span><span class="sxs-lookup"><span data-stu-id="1df85-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="1df85-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1df85-113">PARAMETERS</span></span>

### <span data-ttu-id="1df85-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="1df85-114">-CommandId</span></span>
<span data-ttu-id="1df85-115">A parancs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1df85-115">The command id.</span></span>

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

### <span data-ttu-id="1df85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df85-116">-DefaultProfile</span></span>
<span data-ttu-id="1df85-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1df85-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1df85-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="1df85-118">-Location</span></span>
<span data-ttu-id="1df85-119">A futtatott parancsok lekérdezésének helye.</span><span class="sxs-lookup"><span data-stu-id="1df85-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="1df85-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df85-120">CommonParameters</span></span>
<span data-ttu-id="1df85-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1df85-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df85-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df85-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df85-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1df85-123">INPUTS</span></span>

### <span data-ttu-id="1df85-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1df85-124">System.String</span></span>

## <span data-ttu-id="1df85-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1df85-125">OUTPUTS</span></span>

### <span data-ttu-id="1df85-126">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="1df85-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="1df85-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1df85-127">NOTES</span></span>

## <span data-ttu-id="1df85-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1df85-128">RELATED LINKS</span></span>

