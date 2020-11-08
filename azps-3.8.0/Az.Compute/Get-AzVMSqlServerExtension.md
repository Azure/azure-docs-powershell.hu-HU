---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 7903e13abf7e924898910ad007eefcf6800dcc61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002937"
---
# <span data-ttu-id="c139e-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c139e-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="c139e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c139e-102">SYNOPSIS</span></span>
<span data-ttu-id="c139e-103">A virtuális gép SQL Server-bővítményének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c139e-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="c139e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c139e-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c139e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c139e-105">DESCRIPTION</span></span>
<span data-ttu-id="c139e-106">A **Get-AzVMSqlServerExtension** parancsmag a virtuális GÉPEN az SQL Server-infrastruktúra szolgáltatás (IaaS) ügynökének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c139e-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="c139e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c139e-107">EXAMPLES</span></span>

### <span data-ttu-id="c139e-108">Példa 1: SQL Server-bővítmény beállításainak beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="c139e-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="c139e-109">Ez a parancs a ContosoVM07 nevű virtuális gép SQL Server bővítményének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c139e-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="c139e-110">2. példa: a beállítások beszerzése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="c139e-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="c139e-111">Ez a parancs a ContosoVM22 nevű virtuális gépet az Get-AzVM parancsmag használatával kapja meg a szolgáltatás Service08.</span><span class="sxs-lookup"><span data-stu-id="c139e-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="c139e-112">A parancs a csővezeték-kezelő segítségével átadja az eredményeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c139e-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c139e-113">A jelenlegi parancs a virtuális gépen az SQL Server IaaS-ügynök beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c139e-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="c139e-114">3. példa: adott SQL Server-verzió beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="c139e-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="c139e-115">Ez a parancs a ContosoVM07 nevű virtuális gépen az SQL Server Extension 1,0-as verziójának beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c139e-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="c139e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c139e-116">PARAMETERS</span></span>

### <span data-ttu-id="c139e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c139e-117">-DefaultProfile</span></span>
<span data-ttu-id="c139e-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c139e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c139e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c139e-119">-Name</span></span>
<span data-ttu-id="c139e-120">Annak az SQL Server-kiszolgálónak a nevét adja meg, amely a kiterjesztést adja.</span><span class="sxs-lookup"><span data-stu-id="c139e-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c139e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c139e-121">-ResourceGroupName</span></span>
<span data-ttu-id="c139e-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c139e-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c139e-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="c139e-123">-VMName</span></span>
<span data-ttu-id="c139e-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c139e-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="c139e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c139e-125">CommonParameters</span></span>
<span data-ttu-id="c139e-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c139e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c139e-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c139e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c139e-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c139e-128">INPUTS</span></span>

### <span data-ttu-id="c139e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c139e-129">System.String</span></span>

## <span data-ttu-id="c139e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c139e-130">OUTPUTS</span></span>

### <span data-ttu-id="c139e-131">Microsoft. Azure. commands. kiszámítás. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c139e-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="c139e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c139e-132">NOTES</span></span>

## <span data-ttu-id="c139e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c139e-133">RELATED LINKS</span></span>

[<span data-ttu-id="c139e-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c139e-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c139e-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c139e-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="c139e-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c139e-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


