---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024319"
---
# <span data-ttu-id="23013-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="23013-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="23013-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23013-102">SYNOPSIS</span></span>
<span data-ttu-id="23013-103">Új konfiguráció létrehozása egy virtuális SQL-gépen.</span><span class="sxs-lookup"><span data-stu-id="23013-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="23013-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23013-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23013-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23013-105">DESCRIPTION</span></span>
<span data-ttu-id="23013-106">Az New-AzSqlVMConfig parancsmag létrehoz egy új konfigurációs objektumot egy virtuális SQL-géphez.</span><span class="sxs-lookup"><span data-stu-id="23013-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="23013-107">Példák</span><span class="sxs-lookup"><span data-stu-id="23013-107">EXAMPLES</span></span>

### <span data-ttu-id="23013-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="23013-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="23013-109">Az SQL Virtual Machine helyi konfigurálható objektumát hozza létre, amely az Azure SQL Virtual Machine létrehozása céljából használható.</span><span class="sxs-lookup"><span data-stu-id="23013-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="23013-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23013-110">PARAMETERS</span></span>

### <span data-ttu-id="23013-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23013-111">-DefaultProfile</span></span>
<span data-ttu-id="23013-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23013-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23013-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="23013-113">-LicenseType</span></span>
<span data-ttu-id="23013-114">Virtuális SQL Machine-licenc típusa</span><span class="sxs-lookup"><span data-stu-id="23013-114">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23013-115">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="23013-115">-Offer</span></span>
<span data-ttu-id="23013-116">Virtuális SQL-gép ajánlata.</span><span class="sxs-lookup"><span data-stu-id="23013-116">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23013-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="23013-117">-Sku</span></span>
<span data-ttu-id="23013-118">SQL virtuálisgép-Kiadás típusa</span><span class="sxs-lookup"><span data-stu-id="23013-118">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23013-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="23013-119">-SqlManagementType</span></span>
<span data-ttu-id="23013-120">SQL virtuálisgép-kezelés típusa</span><span class="sxs-lookup"><span data-stu-id="23013-120">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23013-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="23013-121">-Tag</span></span>
<span data-ttu-id="23013-122">Az SQL Virtual Machine-tel társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="23013-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23013-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23013-123">CommonParameters</span></span>
<span data-ttu-id="23013-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23013-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23013-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23013-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23013-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23013-126">INPUTS</span></span>

### <span data-ttu-id="23013-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="23013-127">None</span></span>

## <span data-ttu-id="23013-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23013-128">OUTPUTS</span></span>

### <span data-ttu-id="23013-129">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="23013-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="23013-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23013-130">NOTES</span></span>

## <span data-ttu-id="23013-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23013-131">RELATED LINKS</span></span>
