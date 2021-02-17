---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207839"
---
# <span data-ttu-id="87cc1-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="87cc1-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="87cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="87cc1-103">Új konfigurációt hoz létre egy sql virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="87cc1-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="87cc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87cc1-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87cc1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="87cc1-106">A New-AzSqlVMConfig parancsmag létrehoz egy új konfigurációs objektumot egy sql virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="87cc1-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="87cc1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87cc1-107">EXAMPLES</span></span>

### <span data-ttu-id="87cc1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="87cc1-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="87cc1-109">Egy sql virtuális gép helyi konfigurálható objektumát hozza létre, amely egy Azure sql virtuális gép létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="87cc1-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="87cc1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87cc1-110">PARAMETERS</span></span>

### <span data-ttu-id="87cc1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cc1-111">-DefaultProfile</span></span>
<span data-ttu-id="87cc1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87cc1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87cc1-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="87cc1-113">-LicenseType</span></span>
<span data-ttu-id="87cc1-114">SQL virtuális gép licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="87cc1-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="87cc1-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="87cc1-115">-Offer</span></span>
<span data-ttu-id="87cc1-116">SQL virtuális gépre való ajánlat.</span><span class="sxs-lookup"><span data-stu-id="87cc1-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="87cc1-117">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="87cc1-117">-Sku</span></span>
<span data-ttu-id="87cc1-118">SQL virtuális gép kiadásának típusa.</span><span class="sxs-lookup"><span data-stu-id="87cc1-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="87cc1-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="87cc1-119">-SqlManagementType</span></span>
<span data-ttu-id="87cc1-120">SQL virtuális gépkezelés típusa.</span><span class="sxs-lookup"><span data-stu-id="87cc1-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="87cc1-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="87cc1-121">-Tag</span></span>
<span data-ttu-id="87cc1-122">Az SQL virtuális géphez társítva lévő címkék</span><span class="sxs-lookup"><span data-stu-id="87cc1-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="87cc1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cc1-123">CommonParameters</span></span>
<span data-ttu-id="87cc1-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87cc1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cc1-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87cc1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cc1-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87cc1-126">INPUTS</span></span>

### <span data-ttu-id="87cc1-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="87cc1-127">None</span></span>

## <span data-ttu-id="87cc1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87cc1-128">OUTPUTS</span></span>

### <span data-ttu-id="87cc1-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="87cc1-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="87cc1-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87cc1-130">NOTES</span></span>

## <span data-ttu-id="87cc1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87cc1-131">RELATED LINKS</span></span>
