---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679788"
---
# <span data-ttu-id="237a3-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="237a3-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="237a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="237a3-102">SYNOPSIS</span></span>
<span data-ttu-id="237a3-103">A virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="237a3-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="237a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="237a3-104">SYNTAX</span></span>

### <span data-ttu-id="237a3-105">GeneralizeResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="237a3-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="237a3-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="237a3-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="237a3-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="237a3-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="237a3-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="237a3-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="237a3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="237a3-109">DESCRIPTION</span></span>
<span data-ttu-id="237a3-110">A **set-AzureRmVM** parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="237a3-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="237a3-111">A parancsmag futtatása előtt jelentkezzen be a virtuális gépre, és a Sysprep segítségével készítse elő a merevlemezt.</span><span class="sxs-lookup"><span data-stu-id="237a3-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="237a3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="237a3-112">EXAMPLES</span></span>

### <span data-ttu-id="237a3-113">1. példa: virtuális gép megjelölése általánosként</span><span class="sxs-lookup"><span data-stu-id="237a3-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="237a3-114">Ez a parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="237a3-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="237a3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="237a3-115">PARAMETERS</span></span>

### <span data-ttu-id="237a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237a3-116">-DefaultProfile</span></span>
<span data-ttu-id="237a3-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="237a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="237a3-118">-Általános</span><span class="sxs-lookup"><span data-stu-id="237a3-118">-Generalized</span></span>
<span data-ttu-id="237a3-119">Jelzi, hogy ez a parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="237a3-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237a3-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="237a3-120">-Id</span></span>
<span data-ttu-id="237a3-121">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="237a3-121">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237a3-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="237a3-122">-Name</span></span>
<span data-ttu-id="237a3-123">Annak a virtuális gépnek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="237a3-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237a3-124">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="237a3-124">-Redeploy</span></span>
<span data-ttu-id="237a3-125">Jelzi, hogy ez a parancsmag manuálisan telepíti át a virtuális gépet egy másik Azure-állomásra a problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="237a3-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="237a3-126">Ha újratelepíti a virtuális gépet, az újraindul, ami az elmúló Drive-adatvesztés elvesztésével jár.</span><span class="sxs-lookup"><span data-stu-id="237a3-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237a3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="237a3-127">-ResourceGroupName</span></span>
<span data-ttu-id="237a3-128">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="237a3-128">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237a3-129">CommonParameters</span></span>
<span data-ttu-id="237a3-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="237a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237a3-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="237a3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237a3-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="237a3-132">INPUTS</span></span>

## <span data-ttu-id="237a3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="237a3-133">OUTPUTS</span></span>

## <span data-ttu-id="237a3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="237a3-134">NOTES</span></span>

## <span data-ttu-id="237a3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="237a3-135">RELATED LINKS</span></span>

[<span data-ttu-id="237a3-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="237a3-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


