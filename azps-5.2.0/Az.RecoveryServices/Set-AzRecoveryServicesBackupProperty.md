---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 27b783234f9f38f7445940ceb9969b6bc7fb6273
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357418"
---
# <span data-ttu-id="d9670-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="d9670-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="d9670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9670-102">SYNOPSIS</span></span>
<span data-ttu-id="d9670-103">Beállítja a biztonsági másolatok kezelését.</span><span class="sxs-lookup"><span data-stu-id="d9670-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="d9670-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9670-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9670-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9670-105">DESCRIPTION</span></span>
<span data-ttu-id="d9670-106">A **Set-AzRecoveryServicesBackupProperty** parancsmag beállítja a helyreállítási szolgáltatások tárolója biztonsági mentési tárolási tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d9670-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="d9670-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9670-107">EXAMPLES</span></span>

### <span data-ttu-id="d9670-108">1. példa: GeoRedundant-tároló beállítása egy tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="d9670-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="d9670-109">Az első parancs megkapja a TestVault nevű tárolót, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9670-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="d9670-110">A második parancs georedundánsra állítja a $Vault 01 biztonsági másolat redundanciát.</span><span class="sxs-lookup"><span data-stu-id="d9670-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="d9670-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9670-111">PARAMETERS</span></span>

### <span data-ttu-id="d9670-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="d9670-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="d9670-113">A biztonsági másolat redundanciának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9670-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9670-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9670-114">-DefaultProfile</span></span>
<span data-ttu-id="d9670-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9670-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9670-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="d9670-116">-Vault</span></span>
<span data-ttu-id="d9670-117">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9670-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="d9670-118">A tárolónak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d9670-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="d9670-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9670-119">-Confirm</span></span>
<span data-ttu-id="d9670-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d9670-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9670-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9670-121">-WhatIf</span></span>
<span data-ttu-id="d9670-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d9670-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="d9670-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9670-123">CommonParameters</span></span>
<span data-ttu-id="d9670-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9670-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9670-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9670-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9670-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9670-126">INPUTS</span></span>

### <span data-ttu-id="d9670-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="d9670-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d9670-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9670-128">OUTPUTS</span></span>

### <span data-ttu-id="d9670-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="d9670-129">System.Void</span></span>

## <span data-ttu-id="d9670-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9670-130">NOTES</span></span>

## <span data-ttu-id="d9670-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9670-131">RELATED LINKS</span></span>

[<span data-ttu-id="d9670-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="d9670-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="d9670-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d9670-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


