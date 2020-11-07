---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 9f0f9cfd25e630f0525a724fbec8f8b26ef872db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671335"
---
# <span data-ttu-id="2843a-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2843a-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="2843a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2843a-102">SYNOPSIS</span></span>
<span data-ttu-id="2843a-103">A virtuális gép SQL Server-bővítményének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2843a-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="2843a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2843a-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2843a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2843a-105">DESCRIPTION</span></span>
<span data-ttu-id="2843a-106">A **Get-AzVMSqlServerExtension** parancsmag a virtuális GÉPEN az SQL Server-infrastruktúra szolgáltatás (IaaS) ügynökének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2843a-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="2843a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2843a-107">EXAMPLES</span></span>

### <span data-ttu-id="2843a-108">Példa 1: SQL Server-bővítmény beállításainak beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="2843a-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="2843a-109">Ez a parancs a ContosoVM07 nevű virtuális gép SQL Server bővítményének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2843a-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="2843a-110">2. példa: a beállítások beszerzése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="2843a-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="2843a-111">Ez a parancs a ContosoVM22 nevű virtuális gépet az Get-AzVM parancsmag használatával kapja meg a szolgáltatás Service08.</span><span class="sxs-lookup"><span data-stu-id="2843a-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="2843a-112">A parancs a csővezeték-kezelő segítségével átadja az eredményeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="2843a-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2843a-113">A jelenlegi parancs a virtuális gépen az SQL Server IaaS-ügynök beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2843a-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="2843a-114">3. példa: adott SQL Server-verzió beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="2843a-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="2843a-115">Ez a parancs a ContosoVM07 nevű virtuális gépen az SQL Server Extension 1,0-as verziójának beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2843a-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="2843a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2843a-116">PARAMETERS</span></span>

### <span data-ttu-id="2843a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2843a-117">-DefaultProfile</span></span>
<span data-ttu-id="2843a-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2843a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2843a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2843a-119">-Name</span></span>
<span data-ttu-id="2843a-120">Annak az SQL Server-kiszolgálónak a nevét adja meg, amely a kiterjesztést adja.</span><span class="sxs-lookup"><span data-stu-id="2843a-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="2843a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2843a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2843a-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2843a-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2843a-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="2843a-123">-VMName</span></span>
<span data-ttu-id="2843a-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2843a-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="2843a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2843a-125">CommonParameters</span></span>
<span data-ttu-id="2843a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2843a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2843a-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2843a-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2843a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2843a-128">INPUTS</span></span>

### <span data-ttu-id="2843a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2843a-129">System.String</span></span>

## <span data-ttu-id="2843a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2843a-130">OUTPUTS</span></span>

### <span data-ttu-id="2843a-131">Microsoft. Azure. commands. kiszámítás. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="2843a-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="2843a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2843a-132">NOTES</span></span>

## <span data-ttu-id="2843a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2843a-133">RELATED LINKS</span></span>

[<span data-ttu-id="2843a-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2843a-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2843a-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2843a-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="2843a-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2843a-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


