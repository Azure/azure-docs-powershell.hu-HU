---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 5733939c24437c974f629588106d6240766a9df1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495456"
---
# <span data-ttu-id="1f5c6-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1f5c6-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="1f5c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5c6-103">Információt kap a szakács kibővítéséről.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f5c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f5c6-104">SYNTAX</span></span>

### <span data-ttu-id="1f5c6-105">Linux</span><span class="sxs-lookup"><span data-stu-id="1f5c6-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [<CommonParameters>]
```

### <span data-ttu-id="1f5c6-106">Windows</span><span class="sxs-lookup"><span data-stu-id="1f5c6-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [<CommonParameters>]
```

## <span data-ttu-id="1f5c6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f5c6-107">DESCRIPTION</span></span>
<span data-ttu-id="1f5c6-108">A **Get-AzureVMChefExtension** parancsmag a virtuális gépre telepített Chef-bővítményekről tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="1f5c6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1f5c6-109">EXAMPLES</span></span>

### <span data-ttu-id="1f5c6-110">Példa 1: a séf kibővítésének részletei a Windows Virtual Machine rendszerhez –</span><span class="sxs-lookup"><span data-stu-id="1f5c6-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="1f5c6-111">Ez a parancs a Chef bővítményt egy olyan Windows Virtual Machine-WindowsVM001 kapja, amely az ResourceGroup001 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="1f5c6-112">2. példa: a séf-kiterjesztés részleteinek beszerzése egy linuxos virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="1f5c6-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="1f5c6-113">Ez a parancs a Chef kiterjesztését egy LinuxVM001 nevű linuxos virtuális gépről kapja, amely az ResourceGroup002 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="1f5c6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f5c6-114">PARAMETERS</span></span>

### <span data-ttu-id="1f5c6-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="1f5c6-115">-Linux</span></span>
<span data-ttu-id="1f5c6-116">Jelzi, hogy ez a parancsmag egy linuxos virtuális gépen működik.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-116">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f5c6-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f5c6-117">-Name</span></span>
<span data-ttu-id="1f5c6-118">A Szakácsi mellék nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-118">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="1f5c6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f5c6-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f5c6-120">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="1f5c6-121">-Állapot</span><span class="sxs-lookup"><span data-stu-id="1f5c6-121">-Status</span></span>
<span data-ttu-id="1f5c6-122">Azt jelzi, hogy ez a parancsmag csak a séf bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-122">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="1f5c6-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="1f5c6-123">-VMName</span></span>
<span data-ttu-id="1f5c6-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-124">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="1f5c6-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="1f5c6-125">-Windows</span></span>
<span data-ttu-id="1f5c6-126">Jelzi, hogy ez a parancsmag egy Windows Virtual Machine-géphez van.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-126">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f5c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5c6-127">CommonParameters</span></span>
<span data-ttu-id="1f5c6-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f5c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5c6-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f5c6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5c6-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f5c6-130">INPUTS</span></span>

### <span data-ttu-id="1f5c6-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="1f5c6-131">None</span></span>
<span data-ttu-id="1f5c6-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1f5c6-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f5c6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f5c6-133">OUTPUTS</span></span>

## <span data-ttu-id="1f5c6-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f5c6-134">NOTES</span></span>

## <span data-ttu-id="1f5c6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f5c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="1f5c6-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1f5c6-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="1f5c6-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1f5c6-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


