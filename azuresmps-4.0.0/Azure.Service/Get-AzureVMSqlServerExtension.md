---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015530"
---
# <span data-ttu-id="9aa60-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9aa60-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="9aa60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9aa60-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa60-103">Az SQL Server IaaS ügynök beállításait egy adott virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9aa60-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="9aa60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9aa60-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9aa60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9aa60-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa60-106">A **Get-AzureVMSqlServerExtension** parancsmag egy adott virtuális GÉPEN az SQL Server-infrastruktúra szolgáltatás (IaaS) ügynökének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9aa60-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="9aa60-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9aa60-107">EXAMPLES</span></span>

### <span data-ttu-id="9aa60-108">Példa 1: SQL Server-bővítmény beállításainak beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="9aa60-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9aa60-109">Egy adott virtuális gépen az SQL Server-bővítmény beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9aa60-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="9aa60-110">2. példa: SQL Server-IaaS-ügynök beállításainak beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="9aa60-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9aa60-111">Átadja az SQL Server IaaS-ügynök beállításait egy adott virtuális gépen a vezetékes bemenet használatával.</span><span class="sxs-lookup"><span data-stu-id="9aa60-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="9aa60-112">3. példa: adott SQL Server-IaaS-ügynök beállításainak beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="9aa60-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9aa60-113">Ez a parancs a virtuális gépen az SQL Server IaaS-ügynök adott verziójának beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9aa60-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="9aa60-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9aa60-114">PARAMETERS</span></span>

### <span data-ttu-id="9aa60-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9aa60-115">-InformationAction</span></span>
<span data-ttu-id="9aa60-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="9aa60-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9aa60-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9aa60-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9aa60-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="9aa60-118">Continue</span></span>
- <span data-ttu-id="9aa60-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="9aa60-119">Ignore</span></span>
- <span data-ttu-id="9aa60-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="9aa60-120">Inquire</span></span>
- <span data-ttu-id="9aa60-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9aa60-121">SilentlyContinue</span></span>
- <span data-ttu-id="9aa60-122">állj</span><span class="sxs-lookup"><span data-stu-id="9aa60-122">Stop</span></span>
- <span data-ttu-id="9aa60-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="9aa60-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa60-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9aa60-124">-InformationVariable</span></span>
<span data-ttu-id="9aa60-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="9aa60-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa60-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="9aa60-126">-Profile</span></span>
<span data-ttu-id="9aa60-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9aa60-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9aa60-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9aa60-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa60-129">-VM</span><span class="sxs-lookup"><span data-stu-id="9aa60-129">-VM</span></span>
<span data-ttu-id="9aa60-130">Annak a virtuális gépnek az objektumát adja meg, amelytől a parancsmag a beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="9aa60-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa60-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa60-131">CommonParameters</span></span>
<span data-ttu-id="9aa60-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9aa60-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa60-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa60-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa60-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9aa60-134">INPUTS</span></span>

## <span data-ttu-id="9aa60-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9aa60-135">OUTPUTS</span></span>

## <span data-ttu-id="9aa60-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9aa60-136">NOTES</span></span>

## <span data-ttu-id="9aa60-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9aa60-137">RELATED LINKS</span></span>

[<span data-ttu-id="9aa60-138">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9aa60-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="9aa60-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9aa60-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


