---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: c006c06d03e1f1c120ed62f38ea8b3e451d8fa21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680382"
---
# <span data-ttu-id="f2c2f-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f2c2f-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="f2c2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c2f-103">Engedélyezi a SAP-rendszerek figyelését.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2c2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2c2f-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2c2f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="f2c2f-106">A **set-AzureRmVMAEMExtension** parancsmag frissíti a virtuális gép konfigurációját, hogy engedélyezze vagy frissítse a virtuális GÉPRE telepített SAP-rendszerek figyelésének támogatását.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="f2c2f-107">A parancsmag telepíti az Azure Enhanced monitoring (AEM) bővítményt, amely összegyűjti a teljesítménnyel kapcsolatos adatokat, így az SAP rendszer számára elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="f2c2f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f2c2f-108">EXAMPLES</span></span>

### <span data-ttu-id="f2c2f-109">1. példa: az AEM-bővítmény használata</span><span class="sxs-lookup"><span data-stu-id="f2c2f-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="f2c2f-110">Ez a parancs a contoso-Server nevű virtuális gépet az AEM-bővítmény használatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="f2c2f-111">A parancs a stdstorage nevű tárterület-fiókot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="f2c2f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2c2f-112">PARAMETERS</span></span>

### <span data-ttu-id="f2c2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c2f-113">-DefaultProfile</span></span>
<span data-ttu-id="f2c2f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c2f-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="f2c2f-115">-EnableWAD</span></span>
<span data-ttu-id="f2c2f-116">Ha ez a paraméter meg van határozva, akkor a parancsmagot engedélyezi a Windows Azure Diagnostics for this Virtual Machine használatát.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c2f-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="f2c2f-117">-OSType</span></span>
<span data-ttu-id="f2c2f-118">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-118">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f2c2f-119">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-119">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f2c2f-120">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-120">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="f2c2f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c2f-121">-ResourceGroupName</span></span>
<span data-ttu-id="f2c2f-122">Annak a virtuális gépnek az erőforráscsoport-csoportjának a nevét adja meg, amelyre a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-122">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f2c2f-123">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="f2c2f-123">-SkipStorage</span></span>
<span data-ttu-id="f2c2f-124">Jelzi, hogy ez a parancsmag kihagyja a tárterület konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-124">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c2f-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2c2f-125">-VMName</span></span>
<span data-ttu-id="f2c2f-126">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f2c2f-127">Ez a parancsmag hozzáadja a virtuális gép AEM bővítményét, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-127">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2c2f-128">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f2c2f-128">-WADStorageAccountName</span></span>
<span data-ttu-id="f2c2f-129">Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag a LinuxDiagnostics vagy a IaaSDiagnostics bővítmény konfigurálásához használ.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-129">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="f2c2f-130">Ha a virtuális gép nem szabványos tárolási fiókot használ, meg kell adnia a paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="f2c2f-130">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c2f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c2f-131">CommonParameters</span></span>
<span data-ttu-id="f2c2f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2c2f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c2f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c2f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c2f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2c2f-134">INPUTS</span></span>

### <span data-ttu-id="f2c2f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f2c2f-135">System.String</span></span>

## <span data-ttu-id="f2c2f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2c2f-136">OUTPUTS</span></span>

### <span data-ttu-id="f2c2f-137">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f2c2f-137">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f2c2f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2c2f-138">NOTES</span></span>

## <span data-ttu-id="f2c2f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2c2f-139">RELATED LINKS</span></span>

[<span data-ttu-id="f2c2f-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f2c2f-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f2c2f-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f2c2f-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f2c2f-142">Teszt-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f2c2f-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


