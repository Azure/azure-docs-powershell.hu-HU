---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 5ae237c21c78f206188f23153bdf35c6bea10b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672386"
---
# <span data-ttu-id="a6ba3-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a6ba3-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="a6ba3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ba3-103">Rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6ba3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6ba3-104">SYNTAX</span></span>

### <span data-ttu-id="a6ba3-105">WindowsParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6ba3-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [<CommonParameters>]
```

### <span data-ttu-id="a6ba3-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="a6ba3-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a6ba3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6ba3-107">DESCRIPTION</span></span>
<span data-ttu-id="a6ba3-108">A **Get-AzureRmVMBootDiagnosticsData** parancsmag rendszerindítási diagnosztikai adatot kap egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="a6ba3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a6ba3-109">EXAMPLES</span></span>

### <span data-ttu-id="a6ba3-110">1. példa: a rendszerindítási diagnosztika adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="a6ba3-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="a6ba3-111">Ez a parancs a ContosoVM07 nevű virtuális gép rendszerindítási diagnosztikai értékeit kapja.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="a6ba3-112">Ez a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="a6ba3-113">A parancs a megadott helyi elérési utakban tárolja az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="a6ba3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6ba3-114">PARAMETERS</span></span>

### <span data-ttu-id="a6ba3-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="a6ba3-115">-Linux</span></span>
<span data-ttu-id="a6ba3-116">Azt jelzi, hogy a virtuális gép futtatja a Linux operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-116">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="a6ba3-117">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="a6ba3-117">-LocalPath</span></span>
<span data-ttu-id="a6ba3-118">A rendszerindítási diagnosztika adatainak helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-118">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="a6ba3-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6ba3-119">-Name</span></span>
<span data-ttu-id="a6ba3-120">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag diagnosztikai adatot kap.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-120">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="a6ba3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ba3-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6ba3-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a6ba3-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="a6ba3-123">-Windows</span></span>
<span data-ttu-id="a6ba3-124">Azt jelzi, hogy a virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-124">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="a6ba3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ba3-125">CommonParameters</span></span>
<span data-ttu-id="a6ba3-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6ba3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ba3-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ba3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ba3-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6ba3-128">INPUTS</span></span>

### <span data-ttu-id="a6ba3-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="a6ba3-129">None</span></span>
<span data-ttu-id="a6ba3-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6ba3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6ba3-131">OUTPUTS</span></span>

## <span data-ttu-id="a6ba3-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6ba3-132">NOTES</span></span>

## <span data-ttu-id="a6ba3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6ba3-133">RELATED LINKS</span></span>

[<span data-ttu-id="a6ba3-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a6ba3-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


