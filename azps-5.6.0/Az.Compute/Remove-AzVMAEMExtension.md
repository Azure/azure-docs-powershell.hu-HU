---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 71fcf62049cfb15e830b4c8c5f311c042de55bb9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921394"
---
# <span data-ttu-id="b6e9c-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b6e9c-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="b6e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e9c-103">Eltávolítja az AEM bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="b6e9c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6e9c-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6e9c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="b6e9c-106">A **Remove-AzVMAEMExtension** parancsmag eltávolítja az Azure Enhanced Monitoring (AEM) bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="b6e9c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6e9c-107">EXAMPLES</span></span>

### <span data-ttu-id="b6e9c-108">1. példa: Az AEM-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6e9c-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="b6e9c-109">Ez a parancs eltávolítja a contoso-kiszolgáló nevű virtuális gép AEM-bővítményét.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="b6e9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6e9c-110">PARAMETERS</span></span>

### <span data-ttu-id="b6e9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e9c-111">-DefaultProfile</span></span>
<span data-ttu-id="b6e9c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6e9c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b6e9c-113">-Name</span></span>
<span data-ttu-id="b6e9c-114">Annak a virtuális gépnek a nevét adja meg, amelyből a parancsmag eltávolítja az AEM kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="b6e9c-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b6e9c-115">-NoWait</span></span>
<span data-ttu-id="b6e9c-116">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b6e9c-117">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e9c-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="b6e9c-118">-OSType</span></span>
<span data-ttu-id="b6e9c-119">Az operációs rendszer lemezének típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="b6e9c-120">Ha az operációs rendszer lemezének nincs típusa, meg kell adnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="b6e9c-121">A paraméter elfogadható értékei a következőek: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6e9c-123">Egy virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="b6e9c-124">Ez a parancsmag eltávolítja az AEM bővítményt a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="b6e9c-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="b6e9c-125">-VMName</span></span>
<span data-ttu-id="b6e9c-126">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b6e9c-127">Ez a parancsmag eltávolítja a paraméterrel megadott virtuális gép AEM-bővítményét.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6e9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e9c-128">CommonParameters</span></span>
<span data-ttu-id="b6e9c-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e9c-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6e9c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e9c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6e9c-131">INPUTS</span></span>

### <span data-ttu-id="b6e9c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b6e9c-132">System.String</span></span>

## <span data-ttu-id="b6e9c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e9c-133">OUTPUTS</span></span>

### <span data-ttu-id="b6e9c-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b6e9c-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b6e9c-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6e9c-135">NOTES</span></span>

## <span data-ttu-id="b6e9c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6e9c-136">RELATED LINKS</span></span>

[<span data-ttu-id="b6e9c-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b6e9c-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="b6e9c-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b6e9c-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="b6e9c-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b6e9c-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


