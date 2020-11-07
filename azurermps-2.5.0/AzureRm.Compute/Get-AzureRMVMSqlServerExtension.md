---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 6b02a83c7664fa460cd4ebd25a1754a8bc57e784
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850945"
---
# <span data-ttu-id="57373-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="57373-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="57373-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57373-102">SYNOPSIS</span></span>
<span data-ttu-id="57373-103">A virtuális gép SQL Server-bővítményének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57373-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57373-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57373-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57373-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57373-105">DESCRIPTION</span></span>
<span data-ttu-id="57373-106">A **Get-AzureRmVMSqlServerExtension** parancsmag a virtuális GÉPEN az SQL Server-infrastruktúra szolgáltatás (IaaS) ügynökének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57373-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="57373-107">Példák</span><span class="sxs-lookup"><span data-stu-id="57373-107">EXAMPLES</span></span>

### <span data-ttu-id="57373-108">Példa 1: SQL Server-bővítmény beállításainak beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="57373-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="57373-109">Ez a parancs a ContosoVM07 nevű virtuális gép SQL Server bővítményének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57373-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="57373-110">2. példa: a beállítások beszerzése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="57373-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="57373-111">Ez a parancs a ContosoVM22 nevű virtuális gépet az Get-AzureRmVM parancsmag használatával kapja meg a szolgáltatás Service08.</span><span class="sxs-lookup"><span data-stu-id="57373-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="57373-112">A parancs a csővezeték-kezelő segítségével átadja az eredményeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="57373-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="57373-113">A jelenlegi parancs a virtuális gépen az SQL Server IaaS-ügynök beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57373-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="57373-114">3. példa: adott SQL Server-verzió beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="57373-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="57373-115">Ez a parancs a ContosoVM07 nevű virtuális gépen az SQL Server Extension 1,0-as verziójának beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57373-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="57373-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57373-116">PARAMETERS</span></span>

### <span data-ttu-id="57373-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57373-117">-DefaultProfile</span></span>
<span data-ttu-id="57373-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57373-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57373-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57373-119">-Name</span></span>
<span data-ttu-id="57373-120">Annak az SQL Server-kiszolgálónak a nevét adja meg, amely a kiterjesztést adja.</span><span class="sxs-lookup"><span data-stu-id="57373-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="57373-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57373-121">-ResourceGroupName</span></span>
<span data-ttu-id="57373-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57373-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="57373-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="57373-123">-VMName</span></span>
<span data-ttu-id="57373-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57373-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="57373-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57373-125">CommonParameters</span></span>
<span data-ttu-id="57373-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57373-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57373-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57373-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57373-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57373-128">INPUTS</span></span>

### <span data-ttu-id="57373-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="57373-129">None</span></span>
<span data-ttu-id="57373-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="57373-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57373-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57373-131">OUTPUTS</span></span>

### <span data-ttu-id="57373-132">Microsoft. Azure. commands. kiszámítás. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="57373-132">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="57373-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57373-133">NOTES</span></span>

## <span data-ttu-id="57373-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57373-134">RELATED LINKS</span></span>

[<span data-ttu-id="57373-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="57373-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="57373-136">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="57373-136">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="57373-137">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="57373-137">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


