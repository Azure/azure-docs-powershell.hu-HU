---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181174"
---
# <span data-ttu-id="edd57-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="edd57-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="edd57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="edd57-102">SYNOPSIS</span></span>
<span data-ttu-id="edd57-103">Eltávolítja az agrár-AEM bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="edd57-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="edd57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="edd57-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edd57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="edd57-105">DESCRIPTION</span></span>
<span data-ttu-id="edd57-106">A **Remove-AzVMAEMExtension** parancsmag eltávolítja az Azure Enhanced monitoring (AEM) bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="edd57-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="edd57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="edd57-107">EXAMPLES</span></span>

### <span data-ttu-id="edd57-108">1. példa: az agrár-AEM bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="edd57-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="edd57-109">Ez a parancs eltávolítja a contoso-Server nevű virtuális gép AEM-bővítményét.</span><span class="sxs-lookup"><span data-stu-id="edd57-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="edd57-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="edd57-110">PARAMETERS</span></span>

### <span data-ttu-id="edd57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd57-111">-DefaultProfile</span></span>
<span data-ttu-id="edd57-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edd57-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd57-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="edd57-113">-Name</span></span>
<span data-ttu-id="edd57-114">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az AEM-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="edd57-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="edd57-115">-Várva</span><span class="sxs-lookup"><span data-stu-id="edd57-115">-NoWait</span></span>
<span data-ttu-id="edd57-116">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="edd57-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="edd57-117">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="edd57-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="edd57-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="edd57-118">-OSType</span></span>
<span data-ttu-id="edd57-119">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="edd57-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="edd57-120">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="edd57-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="edd57-121">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="edd57-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="edd57-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd57-122">-ResourceGroupName</span></span>
<span data-ttu-id="edd57-123">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="edd57-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="edd57-124">Ez a parancsmag eltávolítja az agrár-AEM bővítményt a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="edd57-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="edd57-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="edd57-125">-VMName</span></span>
<span data-ttu-id="edd57-126">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="edd57-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="edd57-127">Ez a parancsmag eltávolítja a virtuális gép AEM bővítményét, amelyre ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="edd57-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="edd57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd57-128">CommonParameters</span></span>
<span data-ttu-id="edd57-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="edd57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd57-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="edd57-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd57-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="edd57-131">INPUTS</span></span>

### <span data-ttu-id="edd57-132">System. String</span><span class="sxs-lookup"><span data-stu-id="edd57-132">System.String</span></span>

## <span data-ttu-id="edd57-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edd57-133">OUTPUTS</span></span>

### <span data-ttu-id="edd57-134">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="edd57-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="edd57-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="edd57-135">NOTES</span></span>

## <span data-ttu-id="edd57-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edd57-136">RELATED LINKS</span></span>

[<span data-ttu-id="edd57-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="edd57-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="edd57-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="edd57-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="edd57-139">Teszt-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="edd57-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


