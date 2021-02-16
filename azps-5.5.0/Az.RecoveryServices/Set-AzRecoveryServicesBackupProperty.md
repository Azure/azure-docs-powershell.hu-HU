---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 17187a1a5caa2de3f39ad7153ee1313e4ee8e3e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158531"
---
# <span data-ttu-id="64bf8-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="64bf8-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="64bf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="64bf8-103">Beállítja a tulajdonságokat a biztonsági másolatok kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="64bf8-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="64bf8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64bf8-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>  [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-EnableCrossRegionRestore] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64bf8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="64bf8-106">A **Set-AzRecoveryServicesBackupProperty** parancsmag beállítja a helyreállítási szolgáltatások tárolója biztonsági mentési tárolási tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="64bf8-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="64bf8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="64bf8-108">1. példa: GeoRedundant-tároló beállítása egy tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="64bf8-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="64bf8-109">Az első parancs megkapja a TestVault nevű tárolót, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="64bf8-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="64bf8-110">A második parancs georedundánsra állítja a $Vault 01 biztonsági másolat redundanciát.</span><span class="sxs-lookup"><span data-stu-id="64bf8-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="64bf8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64bf8-111">PARAMETERS</span></span>

### <span data-ttu-id="64bf8-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="64bf8-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="64bf8-113">A biztonsági másolat redundanciának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bf8-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, ZoneRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bf8-114">-DefaultProfile</span></span>
<span data-ttu-id="64bf8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64bf8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64bf8-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="64bf8-116">-Vault</span></span>
<span data-ttu-id="64bf8-117">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bf8-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="64bf8-118">A tárolónak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="64bf8-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64bf8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64bf8-119">-Confirm</span></span>
<span data-ttu-id="64bf8-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64bf8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bf8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64bf8-121">-WhatIf</span></span>
<span data-ttu-id="64bf8-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64bf8-122">Shows what would happen if the cmdlet runs.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bf8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bf8-123">CommonParameters</span></span>
<span data-ttu-id="64bf8-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bf8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bf8-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64bf8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bf8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64bf8-126">INPUTS</span></span>

### <span data-ttu-id="64bf8-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="64bf8-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="64bf8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64bf8-128">OUTPUTS</span></span>

### <span data-ttu-id="64bf8-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="64bf8-129">System.Void</span></span>

## <span data-ttu-id="64bf8-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64bf8-130">NOTES</span></span>

## <span data-ttu-id="64bf8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64bf8-131">RELATED LINKS</span></span>

[<span data-ttu-id="64bf8-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="64bf8-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="64bf8-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="64bf8-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


