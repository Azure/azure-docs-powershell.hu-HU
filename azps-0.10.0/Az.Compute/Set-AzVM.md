---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 236c200c4c3434afa6b848d9fb72821823ad0dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844257"
---
# <span data-ttu-id="de937-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="de937-101">Set-AzVM</span></span>

## <span data-ttu-id="de937-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de937-102">SYNOPSIS</span></span>
<span data-ttu-id="de937-103">A virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="de937-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="de937-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de937-104">SYNTAX</span></span>

### <span data-ttu-id="de937-105">GeneralizeResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de937-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de937-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="de937-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de937-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="de937-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de937-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="de937-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de937-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="de937-109">DESCRIPTION</span></span>
<span data-ttu-id="de937-110">A **set-AzVM** parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="de937-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="de937-111">A parancsmag futtatása előtt jelentkezzen be a virtuális gépre, és a Sysprep segítségével készítse elő a merevlemezt.</span><span class="sxs-lookup"><span data-stu-id="de937-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="de937-112">Példák</span><span class="sxs-lookup"><span data-stu-id="de937-112">EXAMPLES</span></span>

### <span data-ttu-id="de937-113">1. példa: virtuális gép megjelölése általánosként</span><span class="sxs-lookup"><span data-stu-id="de937-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="de937-114">Ez a parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="de937-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="de937-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de937-115">PARAMETERS</span></span>

### <span data-ttu-id="de937-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de937-116">-AsJob</span></span>
<span data-ttu-id="de937-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="de937-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de937-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de937-118">-DefaultProfile</span></span>
<span data-ttu-id="de937-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de937-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de937-120">-Általános</span><span class="sxs-lookup"><span data-stu-id="de937-120">-Generalized</span></span>
<span data-ttu-id="de937-121">Jelzi, hogy ez a parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="de937-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de937-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="de937-122">-Id</span></span>
<span data-ttu-id="de937-123">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="de937-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de937-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de937-124">-Name</span></span>
<span data-ttu-id="de937-125">Annak a virtuális gépnek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="de937-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="de937-126">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="de937-126">-Redeploy</span></span>
<span data-ttu-id="de937-127">Jelzi, hogy ez a parancsmag manuálisan telepíti át a virtuális gépet egy másik Azure-állomásra a problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="de937-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="de937-128">Ha újratelepíti a virtuális gépet, az újraindul, ami az elmúló Drive-adatvesztés elvesztésével jár.</span><span class="sxs-lookup"><span data-stu-id="de937-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de937-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de937-129">-ResourceGroupName</span></span>
<span data-ttu-id="de937-130">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de937-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de937-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de937-131">CommonParameters</span></span>
<span data-ttu-id="de937-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de937-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de937-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de937-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de937-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de937-134">INPUTS</span></span>

### <span data-ttu-id="de937-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="de937-135">None</span></span>
<span data-ttu-id="de937-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="de937-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de937-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de937-137">OUTPUTS</span></span>

### <span data-ttu-id="de937-138">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="de937-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="de937-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de937-139">NOTES</span></span>

## <span data-ttu-id="de937-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de937-140">RELATED LINKS</span></span>

[<span data-ttu-id="de937-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="de937-141">Get-AzVM</span></span>](./Get-AzVM.md)


