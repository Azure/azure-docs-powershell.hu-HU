---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: 01eb8cba77177ca35f2e1b73ec410baa44e4a58c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848493"
---
# <span data-ttu-id="e70d9-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e70d9-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="e70d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e70d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e70d9-103">Engedélyezi a SAP-rendszerek figyelését.</span><span class="sxs-lookup"><span data-stu-id="e70d9-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e70d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e70d9-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e70d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e70d9-105">DESCRIPTION</span></span>
<span data-ttu-id="e70d9-106">A **set-AzureRmVMAEMExtension** parancsmag frissíti a virtuális gép konfigurációját, hogy engedélyezze vagy frissítse a virtuális GÉPRE telepített SAP-rendszerek figyelésének támogatását.</span><span class="sxs-lookup"><span data-stu-id="e70d9-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="e70d9-107">A parancsmag telepíti az Azure Enhanced monitoring (AEM) bővítményt, amely összegyűjti a teljesítménnyel kapcsolatos adatokat, így az SAP rendszer számára elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="e70d9-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="e70d9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e70d9-108">EXAMPLES</span></span>

### <span data-ttu-id="e70d9-109">1. példa: az AEM-bővítmény használata</span><span class="sxs-lookup"><span data-stu-id="e70d9-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="e70d9-110">Ez a parancs a contoso-Server nevű virtuális gépet az AEM-bővítmény használatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="e70d9-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="e70d9-111">A parancs a stdstorage nevű tárterület-fiókot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70d9-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="e70d9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e70d9-112">PARAMETERS</span></span>

### <span data-ttu-id="e70d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70d9-113">-DefaultProfile</span></span>
<span data-ttu-id="e70d9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e70d9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e70d9-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="e70d9-115">-DisableWAD</span></span>
<span data-ttu-id="e70d9-116">Jelzi, hogy ez a parancsmag nem engedélyezi az Azure Diagnostics használatát a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="e70d9-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="e70d9-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="e70d9-117">-EnableWAD</span></span>
<span data-ttu-id="e70d9-118">Ha ez a paraméter meg van határozva, akkor a parancsmagot engedélyezi a Windows Azure Diagnostics for this Virtual Machine használatát.</span><span class="sxs-lookup"><span data-stu-id="e70d9-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70d9-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="e70d9-119">-OSType</span></span>
<span data-ttu-id="e70d9-120">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="e70d9-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="e70d9-121">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="e70d9-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="e70d9-122">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="e70d9-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="e70d9-124">Annak a virtuális gépnek az erőforráscsoport-csoportjának a nevét adja meg, amelyre a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="e70d9-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e70d9-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="e70d9-125">-SkipStorage</span></span>
<span data-ttu-id="e70d9-126">Jelzi, hogy ez a parancsmag kihagyja a tárterület konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e70d9-126">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70d9-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="e70d9-127">-VMName</span></span>
<span data-ttu-id="e70d9-128">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70d9-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e70d9-129">Ez a parancsmag hozzáadja a virtuális gép AEM bővítményét, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="e70d9-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="e70d9-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e70d9-130">-WADStorageAccountName</span></span>
<span data-ttu-id="e70d9-131">Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag a LinuxDiagnostics vagy a IaaSDiagnostics bővítmény konfigurálásához használ.</span><span class="sxs-lookup"><span data-stu-id="e70d9-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="e70d9-132">Ha a virtuális gép nem szabványos tárolási fiókot használ, meg kell adnia a paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="e70d9-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70d9-133">CommonParameters</span></span>
<span data-ttu-id="e70d9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e70d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70d9-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e70d9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70d9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e70d9-136">INPUTS</span></span>

### <span data-ttu-id="e70d9-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="e70d9-137">None</span></span>
<span data-ttu-id="e70d9-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e70d9-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e70d9-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e70d9-139">OUTPUTS</span></span>

### <span data-ttu-id="e70d9-140">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e70d9-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e70d9-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e70d9-141">NOTES</span></span>

## <span data-ttu-id="e70d9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e70d9-142">RELATED LINKS</span></span>

[<span data-ttu-id="e70d9-143">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e70d9-143">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="e70d9-144">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e70d9-144">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="e70d9-145">Teszt-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e70d9-145">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


