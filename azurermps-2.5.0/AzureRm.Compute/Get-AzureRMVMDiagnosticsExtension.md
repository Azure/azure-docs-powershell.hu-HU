---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: e02c86407326d9ea5b12a5a589e5860c9dfb5c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850946"
---
# <span data-ttu-id="68a7c-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="68a7c-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="68a7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="68a7c-103">A diagnosztikai bővítmény beállításait egy virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="68a7c-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68a7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68a7c-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68a7c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68a7c-105">DESCRIPTION</span></span>
<span data-ttu-id="68a7c-106">A **Get-AzureRmVMDiagnosticsExtension** parancsmag a virtuális gépen az Azure Diagnostics bővítmény beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="68a7c-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="68a7c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68a7c-107">EXAMPLES</span></span>

### <span data-ttu-id="68a7c-108">Példa 1: a diagnosztika bővítmény beszerzése virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="68a7c-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="68a7c-109">Ez a parancs beilleszti a ContosoVM22 nevű virtuális gépre a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="68a7c-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="68a7c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68a7c-110">PARAMETERS</span></span>

### <span data-ttu-id="68a7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a7c-111">-DefaultProfile</span></span>
<span data-ttu-id="68a7c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68a7c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68a7c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68a7c-113">-Name</span></span>
<span data-ttu-id="68a7c-114">Annak a diagnosztikai bővítménynek a neve, amelyhez a parancsmag beállításai vannak.</span><span class="sxs-lookup"><span data-stu-id="68a7c-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68a7c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a7c-115">-ResourceGroupName</span></span>
<span data-ttu-id="68a7c-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68a7c-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68a7c-117">-Állapot</span><span class="sxs-lookup"><span data-stu-id="68a7c-117">-Status</span></span>
<span data-ttu-id="68a7c-118">Azt jelzi, hogy ez a parancsmag az állapot értékét használja.</span><span class="sxs-lookup"><span data-stu-id="68a7c-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68a7c-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="68a7c-119">-VMName</span></span>
<span data-ttu-id="68a7c-120">Annak a virtuális gépnek a neve, amelyből a parancsmag a diagnosztika bővítményt kapja.</span><span class="sxs-lookup"><span data-stu-id="68a7c-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68a7c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a7c-121">CommonParameters</span></span>
<span data-ttu-id="68a7c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68a7c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a7c-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a7c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a7c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68a7c-124">INPUTS</span></span>

### <span data-ttu-id="68a7c-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="68a7c-125">None</span></span>
<span data-ttu-id="68a7c-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="68a7c-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68a7c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68a7c-127">OUTPUTS</span></span>

### <span data-ttu-id="68a7c-128">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="68a7c-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="68a7c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68a7c-129">NOTES</span></span>

## <span data-ttu-id="68a7c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68a7c-130">RELATED LINKS</span></span>

[<span data-ttu-id="68a7c-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="68a7c-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="68a7c-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="68a7c-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


