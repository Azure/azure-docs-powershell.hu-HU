---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194488"
---
# <span data-ttu-id="38406-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="38406-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="38406-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38406-102">SYNOPSIS</span></span>
<span data-ttu-id="38406-103">Egy vagy több SQL virtuális gépet kap.</span><span class="sxs-lookup"><span data-stu-id="38406-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="38406-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38406-104">SYNTAX</span></span>

### <span data-ttu-id="38406-105">ResourceGroupOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38406-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38406-106">név</span><span class="sxs-lookup"><span data-stu-id="38406-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38406-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38406-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38406-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="38406-108">DESCRIPTION</span></span>
<span data-ttu-id="38406-109">A Get-AzSqlVM parancsmag egy vagy több SQL virtuális gépet kap.</span><span class="sxs-lookup"><span data-stu-id="38406-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="38406-110">Példák</span><span class="sxs-lookup"><span data-stu-id="38406-110">EXAMPLES</span></span>

### <span data-ttu-id="38406-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="38406-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="38406-112">Ez a parancs az aktuális előfizetésben található összes Azure SQL-gépen információt kap.</span><span class="sxs-lookup"><span data-stu-id="38406-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="38406-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="38406-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="38406-114">Ez a parancs információt kap az összes Azure SQL-gépen az aktuális előfizetésben, amely az erőforráscsoport ResourceGroup01 van társítva.</span><span class="sxs-lookup"><span data-stu-id="38406-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="38406-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="38406-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="38406-116">Ez a parancs információt kap az erőforráscsoport ResourceGroup01 rendelt virtuális virtuális gép "VM" rendszeréről.</span><span class="sxs-lookup"><span data-stu-id="38406-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="38406-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38406-117">PARAMETERS</span></span>

### <span data-ttu-id="38406-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38406-118">-DefaultProfile</span></span>
<span data-ttu-id="38406-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38406-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38406-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38406-120">-Name</span></span>
<span data-ttu-id="38406-121">Az SQL virtuális gép neve</span><span class="sxs-lookup"><span data-stu-id="38406-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38406-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38406-122">-ResourceGroupName</span></span>
<span data-ttu-id="38406-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="38406-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38406-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38406-124">-ResourceId</span></span>
<span data-ttu-id="38406-125">SQL virtuális gép erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="38406-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38406-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38406-126">CommonParameters</span></span>
<span data-ttu-id="38406-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38406-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38406-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="38406-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38406-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38406-129">INPUTS</span></span>

### <span data-ttu-id="38406-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="38406-130">None</span></span>

## <span data-ttu-id="38406-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38406-131">OUTPUTS</span></span>

### <span data-ttu-id="38406-132">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="38406-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="38406-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38406-133">NOTES</span></span>

## <span data-ttu-id="38406-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38406-134">RELATED LINKS</span></span>
