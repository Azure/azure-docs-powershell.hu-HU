---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
ms.openlocfilehash: 867f2c14e90eddd9649e0720d41f56aa896c61ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848894"
---
# <span data-ttu-id="0bbcd-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0bbcd-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="0bbcd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0bbcd-102">SYNOPSIS</span></span>
<span data-ttu-id="0bbcd-103">Rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bbcd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0bbcd-104">SYNTAX</span></span>

### <span data-ttu-id="0bbcd-105">WindowsParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0bbcd-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bbcd-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="0bbcd-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bbcd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0bbcd-107">DESCRIPTION</span></span>
<span data-ttu-id="0bbcd-108">A **Get-AzureRmVMBootDiagnosticsData** parancsmag rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="0bbcd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0bbcd-109">EXAMPLES</span></span>

### <span data-ttu-id="0bbcd-110">1. példa: a rendszerindítási diagnosztika adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="0bbcd-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="0bbcd-111">Ez a parancs a ContosoVM07 nevű virtuális gép rendszerindítási diagnosztikai értékeit kapja.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="0bbcd-112">Ez a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="0bbcd-113">A parancs a megadott helyi elérési utakban tárolja az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="0bbcd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0bbcd-114">PARAMETERS</span></span>

### <span data-ttu-id="0bbcd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bbcd-115">-DefaultProfile</span></span>
<span data-ttu-id="0bbcd-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bbcd-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0bbcd-117">-Linux</span></span>
<span data-ttu-id="0bbcd-118">Azt jelzi, hogy a virtuális gép futtatja a Linux operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bbcd-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="0bbcd-119">-LocalPath</span></span>
<span data-ttu-id="0bbcd-120">A rendszerindítási diagnosztika adatainak helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbcd-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0bbcd-121">-Name</span></span>
<span data-ttu-id="0bbcd-122">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag diagnosztikai adatot kap.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbcd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbcd-123">-ResourceGroupName</span></span>
<span data-ttu-id="0bbcd-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0bbcd-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="0bbcd-125">-Windows</span></span>
<span data-ttu-id="0bbcd-126">Azt jelzi, hogy a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bbcd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bbcd-127">CommonParameters</span></span>
<span data-ttu-id="0bbcd-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0bbcd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bbcd-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bbcd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bbcd-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bbcd-130">INPUTS</span></span>

### <span data-ttu-id="0bbcd-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="0bbcd-131">None</span></span>
<span data-ttu-id="0bbcd-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0bbcd-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0bbcd-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bbcd-133">OUTPUTS</span></span>

### <span data-ttu-id="0bbcd-134">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0bbcd-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0bbcd-135">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="0bbcd-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="0bbcd-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0bbcd-136">NOTES</span></span>

## <span data-ttu-id="0bbcd-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bbcd-137">RELATED LINKS</span></span>

[<span data-ttu-id="0bbcd-138">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0bbcd-138">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


