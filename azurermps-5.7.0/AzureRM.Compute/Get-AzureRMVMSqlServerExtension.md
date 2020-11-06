---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a6f2ed82835cca252f905cb53c5ddd9c8530900a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503859"
---
# <span data-ttu-id="c5024-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c5024-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="c5024-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5024-102">SYNOPSIS</span></span>
<span data-ttu-id="c5024-103">A virtuális gép SQL Server-bővítményének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5024-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5024-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5024-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5024-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5024-105">DESCRIPTION</span></span>
<span data-ttu-id="c5024-106">A **Get-AzureRmVMSqlServerExtension** parancsmag a virtuális GÉPEN az SQL Server-infrastruktúra szolgáltatás (IaaS) ügynökének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5024-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="c5024-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c5024-107">EXAMPLES</span></span>

### <span data-ttu-id="c5024-108">Példa 1: SQL Server-bővítmény beállításainak beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="c5024-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="c5024-109">Ez a parancs a ContosoVM07 nevű virtuális gép SQL Server bővítményének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5024-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="c5024-110">2. példa: a beállítások beszerzése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="c5024-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="c5024-111">Ez a parancs a ContosoVM22 nevű virtuális gépet az Get-AzureRmVM parancsmag használatával kapja meg a szolgáltatás Service08.</span><span class="sxs-lookup"><span data-stu-id="c5024-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="c5024-112">A parancs a csővezeték-kezelő segítségével átadja az eredményeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c5024-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="c5024-113">A jelenlegi parancs a virtuális gépen az SQL Server IaaS-ügynök beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5024-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="c5024-114">3. példa: adott SQL Server-verzió beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="c5024-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="c5024-115">Ez a parancs a ContosoVM07 nevű virtuális gépen az SQL Server Extension 1,0-as verziójának beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5024-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="c5024-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5024-116">PARAMETERS</span></span>

### <span data-ttu-id="c5024-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5024-117">-Name</span></span>
<span data-ttu-id="c5024-118">Annak az SQL Server-kiszolgálónak a nevét adja meg, amely a kiterjesztést adja.</span><span class="sxs-lookup"><span data-stu-id="c5024-118">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5024-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5024-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5024-120">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5024-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c5024-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="c5024-121">-VMName</span></span>
<span data-ttu-id="c5024-122">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5024-122">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5024-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5024-123">CommonParameters</span></span>
<span data-ttu-id="c5024-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5024-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5024-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5024-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5024-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5024-126">INPUTS</span></span>

### <span data-ttu-id="c5024-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="c5024-127">None</span></span>
<span data-ttu-id="c5024-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c5024-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5024-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5024-129">OUTPUTS</span></span>

## <span data-ttu-id="c5024-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5024-130">NOTES</span></span>

## <span data-ttu-id="c5024-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5024-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5024-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5024-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="c5024-133">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c5024-133">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="c5024-134">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c5024-134">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


