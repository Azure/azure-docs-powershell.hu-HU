---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 846c27dc521e13cb2814a4f9e004325da4263bf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669608"
---
# <span data-ttu-id="b98a3-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="b98a3-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="b98a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b98a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b98a3-103">A helyreállítási szolgáltatások Vault-környezetének beállítása az aktuális PowerShell-munkamenet további Azure-webhely-helyreállítási műveleteihez való használatra.</span><span class="sxs-lookup"><span data-stu-id="b98a3-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="b98a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b98a3-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b98a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b98a3-105">DESCRIPTION</span></span>
<span data-ttu-id="b98a3-106">A **set-AzRecoveryServicesAsrVaultContext** parancsmag az Azure webhely-helyreállítási boltozat környezetének beállításával további műveleteket végezhet.</span><span class="sxs-lookup"><span data-stu-id="b98a3-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="b98a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b98a3-107">EXAMPLES</span></span>

### <span data-ttu-id="b98a3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b98a3-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="b98a3-109">A boltozat környezetének beállítása a megadott helyreállítási szolgáltatások boltozatára az aktuális PowerShell-munkamenetben a további Azure-webhely-helyreállítási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="b98a3-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="b98a3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b98a3-110">PARAMETERS</span></span>

### <span data-ttu-id="b98a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b98a3-111">-DefaultProfile</span></span>
<span data-ttu-id="b98a3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b98a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b98a3-113">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="b98a3-113">-Vault</span></span>
<span data-ttu-id="b98a3-114">A helyreállítási szolgáltatások Vault-objektuma, amely megfelel a helyreállítási szolgáltatások boltozatának.</span><span class="sxs-lookup"><span data-stu-id="b98a3-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="b98a3-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b98a3-115">-Confirm</span></span>
<span data-ttu-id="b98a3-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b98a3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b98a3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b98a3-117">-WhatIf</span></span>
<span data-ttu-id="b98a3-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b98a3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b98a3-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b98a3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b98a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b98a3-120">CommonParameters</span></span>
<span data-ttu-id="b98a3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b98a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b98a3-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b98a3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b98a3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b98a3-123">INPUTS</span></span>

### <span data-ttu-id="b98a3-124">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="b98a3-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b98a3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b98a3-125">OUTPUTS</span></span>

### <span data-ttu-id="b98a3-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b98a3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b98a3-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b98a3-127">NOTES</span></span>

## <span data-ttu-id="b98a3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b98a3-128">RELATED LINKS</span></span>
