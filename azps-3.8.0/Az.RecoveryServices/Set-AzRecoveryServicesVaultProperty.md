---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013521"
---
# <span data-ttu-id="5360b-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="5360b-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="5360b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5360b-102">SYNOPSIS</span></span>
<span data-ttu-id="5360b-103">A boltozat tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="5360b-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="5360b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5360b-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5360b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5360b-105">DESCRIPTION</span></span>
<span data-ttu-id="5360b-106">A **set-AzRecoveryServicesVaultProperty** parancsmag a helyreállítási szolgáltatások boltozatának tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="5360b-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="5360b-107">A **set-AzRecoveryServicesVaultProperty** parancsmaggal a boltozat aktuális tulajdonságait érheti el.</span><span class="sxs-lookup"><span data-stu-id="5360b-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="5360b-108">Ezzel a parancsmaggal a **SoftDeleteFeatureState** tulajdonsága bármely időpontban engedélyezhető.</span><span class="sxs-lookup"><span data-stu-id="5360b-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="5360b-109">A **SoftDeleteFeatureState** tulajdonság csak akkor tiltható le, ha a boltozat nem tartalmaz regisztrált tárolókat.</span><span class="sxs-lookup"><span data-stu-id="5360b-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="5360b-110">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="5360b-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5360b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5360b-111">EXAMPLES</span></span>

### <span data-ttu-id="5360b-112">Példa 1: a boltozat SoftDeleteFeatureState frissítése</span><span class="sxs-lookup"><span data-stu-id="5360b-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="5360b-113">Az első parancs a boltozat objektumot kapja, majd a $vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5360b-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="5360b-114">A második parancs frissíti a boltozat SoftDeleteFeatureState tulajdonságát "enabled" állapotra.</span><span class="sxs-lookup"><span data-stu-id="5360b-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="5360b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5360b-115">PARAMETERS</span></span>

### <span data-ttu-id="5360b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5360b-116">-DefaultProfile</span></span>
<span data-ttu-id="5360b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5360b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5360b-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="5360b-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="5360b-119">SoftDeleteFeatureState a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="5360b-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5360b-120">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5360b-120">-VaultId</span></span>
<span data-ttu-id="5360b-121">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="5360b-121">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5360b-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5360b-122">-Confirm</span></span>
<span data-ttu-id="5360b-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5360b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5360b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5360b-124">-WhatIf</span></span>
<span data-ttu-id="5360b-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5360b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5360b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5360b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5360b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5360b-127">CommonParameters</span></span>
<span data-ttu-id="5360b-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5360b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5360b-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5360b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5360b-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5360b-130">INPUTS</span></span>

### <span data-ttu-id="5360b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5360b-131">System.String</span></span>

### <span data-ttu-id="5360b-132">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="5360b-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="5360b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5360b-133">OUTPUTS</span></span>

### <span data-ttu-id="5360b-134">Microsoft. Azure. Management. RecoveryServices. backup. models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="5360b-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="5360b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5360b-135">NOTES</span></span>

## <span data-ttu-id="5360b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5360b-136">RELATED LINKS</span></span>

[<span data-ttu-id="5360b-137">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5360b-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="5360b-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="5360b-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


