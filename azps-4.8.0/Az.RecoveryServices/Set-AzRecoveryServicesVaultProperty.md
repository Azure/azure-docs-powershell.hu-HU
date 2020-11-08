---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184013"
---
# <span data-ttu-id="762ac-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="762ac-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="762ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="762ac-102">SYNOPSIS</span></span>
<span data-ttu-id="762ac-103">A boltozat tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="762ac-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="762ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="762ac-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="762ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="762ac-105">DESCRIPTION</span></span>
<span data-ttu-id="762ac-106">A **set-AzRecoveryServicesVaultProperty** parancsmag a helyreállítási szolgáltatások boltozatának tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="762ac-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="762ac-107">Ez a parancsmag az aktuális készlet művelet után a frissített Vault-tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="762ac-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="762ac-108">Ezzel a parancsmag-tulajdonsággal (például a finom törléssel) bármikor engedélyezhető a boltozat.</span><span class="sxs-lookup"><span data-stu-id="762ac-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="762ac-109">A **SoftDeleteFeatureState** tulajdonság csak akkor tiltható le, ha a boltozat nem tartalmaz regisztrált tárolókat.</span><span class="sxs-lookup"><span data-stu-id="762ac-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="762ac-110">Példák</span><span class="sxs-lookup"><span data-stu-id="762ac-110">EXAMPLES</span></span>

### <span data-ttu-id="762ac-111">Példa 1: a boltozat SoftDeleteFeatureState frissítése</span><span class="sxs-lookup"><span data-stu-id="762ac-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="762ac-112">Az első parancs a boltozat objektumot kapja, majd a $vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="762ac-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="762ac-113">A második parancs frissíti a boltozat SoftDeleteFeatureState tulajdonságát "enabled" állapotra.</span><span class="sxs-lookup"><span data-stu-id="762ac-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="762ac-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="762ac-114">PARAMETERS</span></span>

### <span data-ttu-id="762ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762ac-115">-DefaultProfile</span></span>
<span data-ttu-id="762ac-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="762ac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="762ac-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="762ac-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="762ac-118">SoftDeleteFeatureState a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="762ac-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="762ac-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="762ac-119">-VaultId</span></span>
<span data-ttu-id="762ac-120">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="762ac-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="762ac-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="762ac-121">-Confirm</span></span>
<span data-ttu-id="762ac-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="762ac-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="762ac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762ac-123">-WhatIf</span></span>
<span data-ttu-id="762ac-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="762ac-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="762ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762ac-125">CommonParameters</span></span>
<span data-ttu-id="762ac-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="762ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762ac-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="762ac-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762ac-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="762ac-128">INPUTS</span></span>

### <span data-ttu-id="762ac-129">System. String</span><span class="sxs-lookup"><span data-stu-id="762ac-129">System.String</span></span>

### <span data-ttu-id="762ac-130">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="762ac-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="762ac-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="762ac-131">OUTPUTS</span></span>

### <span data-ttu-id="762ac-132">Microsoft. Azure. Management. RecoveryServices. backup. models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="762ac-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="762ac-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="762ac-133">NOTES</span></span>

## <span data-ttu-id="762ac-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="762ac-134">RELATED LINKS</span></span>

[<span data-ttu-id="762ac-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="762ac-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="762ac-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="762ac-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


