---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 2aa0c6516614adb5fae84e2d141cf1882de71628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680906"
---
# <span data-ttu-id="0a27a-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0a27a-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="0a27a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a27a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a27a-103">Információt kap a szakács kibővítéséről.</span><span class="sxs-lookup"><span data-stu-id="0a27a-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a27a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a27a-104">SYNTAX</span></span>

### <span data-ttu-id="0a27a-105">Linux</span><span class="sxs-lookup"><span data-stu-id="0a27a-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a27a-106">Windows</span><span class="sxs-lookup"><span data-stu-id="0a27a-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a27a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a27a-107">DESCRIPTION</span></span>
<span data-ttu-id="0a27a-108">A **Get-AzureVMChefExtension** parancsmag a virtuális gépre telepített Chef-bővítményekről tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="0a27a-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="0a27a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0a27a-109">EXAMPLES</span></span>

### <span data-ttu-id="0a27a-110">Példa 1: a séf kibővítésének részletei a Windows Virtual Machine rendszerhez –</span><span class="sxs-lookup"><span data-stu-id="0a27a-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="0a27a-111">Ez a parancs a Chef bővítményt egy olyan Windows Virtual Machine-WindowsVM001 kapja, amely az ResourceGroup001 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="0a27a-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="0a27a-112">2. példa: a séf-kiterjesztés részleteinek beszerzése egy linuxos virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="0a27a-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="0a27a-113">Ez a parancs a Chef kiterjesztését egy LinuxVM001 nevű linuxos virtuális gépről kapja, amely az ResourceGroup002 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="0a27a-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="0a27a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a27a-114">PARAMETERS</span></span>

### <span data-ttu-id="0a27a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a27a-115">-DefaultProfile</span></span>
<span data-ttu-id="0a27a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a27a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a27a-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0a27a-117">-Linux</span></span>
<span data-ttu-id="0a27a-118">Jelzi, hogy ez a parancsmag egy linuxos virtuális gépen működik.</span><span class="sxs-lookup"><span data-stu-id="0a27a-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a27a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a27a-119">-Name</span></span>
<span data-ttu-id="0a27a-120">A Szakácsi mellék nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a27a-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a27a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a27a-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a27a-122">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a27a-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="0a27a-123">-Állapot</span><span class="sxs-lookup"><span data-stu-id="0a27a-123">-Status</span></span>
<span data-ttu-id="0a27a-124">Azt jelzi, hogy ez a parancsmag csak a séf bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0a27a-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a27a-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="0a27a-125">-VMName</span></span>
<span data-ttu-id="0a27a-126">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a27a-126">Specifies the name of a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a27a-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="0a27a-127">-Windows</span></span>
<span data-ttu-id="0a27a-128">Jelzi, hogy ez a parancsmag egy Windows Virtual Machine-géphez van.</span><span class="sxs-lookup"><span data-stu-id="0a27a-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a27a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a27a-129">CommonParameters</span></span>
<span data-ttu-id="0a27a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a27a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a27a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a27a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a27a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a27a-132">INPUTS</span></span>

## <span data-ttu-id="0a27a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a27a-133">OUTPUTS</span></span>

## <span data-ttu-id="0a27a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a27a-134">NOTES</span></span>

## <span data-ttu-id="0a27a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a27a-135">RELATED LINKS</span></span>

[<span data-ttu-id="0a27a-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0a27a-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="0a27a-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0a27a-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


