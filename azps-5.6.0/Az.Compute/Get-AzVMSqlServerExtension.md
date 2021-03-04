---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: e8b09473cc08f7e419488112d5cabb788e622726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933073"
---
# <span data-ttu-id="868ff-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="868ff-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="868ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="868ff-102">SYNOPSIS</span></span>
<span data-ttu-id="868ff-103">Egy SQL Server-bővítmény beállításait kapja meg egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="868ff-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="868ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="868ff-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="868ff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="868ff-105">DESCRIPTION</span></span>
<span data-ttu-id="868ff-106">A **Get-AzVMSqlServerExtension** parancsmag az SQL Server-infrastruktúra (IaaS) ügynökének beállításait kapja meg egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="868ff-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="868ff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="868ff-107">EXAMPLES</span></span>

### <span data-ttu-id="868ff-108">1. példa: SQL Server-bővítmény beállításainak lekérte virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="868ff-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="868ff-109">Ez a parancs az SQL Server-bővítmény beállításait egy ContosoVM07 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="868ff-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="868ff-110">2. példa: A beállítások be szereznie a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="868ff-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="868ff-111">Ez a parancs a ContosoVM22 nevű virtuális gépet a Service08 szolgáltatásban a Get-AzVM parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="868ff-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="868ff-112">A parancs a folyamat műveleti operátorával átadja az eredményeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="868ff-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="868ff-113">Az aktuális parancs az SQL Server IaaS-ügynök beállításait kapja meg a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="868ff-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="868ff-114">3. példa: Adott SQL Server-verzió beállításainak lekérte</span><span class="sxs-lookup"><span data-stu-id="868ff-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="868ff-115">Ez a parancs az SQL Server-bővítmény 1.0-s verziójának beállításait kapja meg egy ContosoVM07 nevű virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="868ff-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="868ff-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="868ff-116">PARAMETERS</span></span>

### <span data-ttu-id="868ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="868ff-117">-DefaultProfile</span></span>
<span data-ttu-id="868ff-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="868ff-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="868ff-119">-Name</span><span class="sxs-lookup"><span data-stu-id="868ff-119">-Name</span></span>
<span data-ttu-id="868ff-120">Az SQL Server bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="868ff-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="868ff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="868ff-121">-ResourceGroupName</span></span>
<span data-ttu-id="868ff-122">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="868ff-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="868ff-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="868ff-123">-VMName</span></span>
<span data-ttu-id="868ff-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="868ff-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="868ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868ff-125">CommonParameters</span></span>
<span data-ttu-id="868ff-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="868ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868ff-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="868ff-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868ff-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="868ff-128">INPUTS</span></span>

### <span data-ttu-id="868ff-129">System.String</span><span class="sxs-lookup"><span data-stu-id="868ff-129">System.String</span></span>

## <span data-ttu-id="868ff-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="868ff-130">OUTPUTS</span></span>

### <span data-ttu-id="868ff-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="868ff-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="868ff-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="868ff-132">NOTES</span></span>

## <span data-ttu-id="868ff-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="868ff-133">RELATED LINKS</span></span>

[<span data-ttu-id="868ff-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="868ff-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="868ff-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="868ff-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="868ff-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="868ff-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


