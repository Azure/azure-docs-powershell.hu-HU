---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181461"
---
# <span data-ttu-id="ef417-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="ef417-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="ef417-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef417-102">SYNOPSIS</span></span>
<span data-ttu-id="ef417-103">A helyreállítási szolgáltatások Vault-környezetének beállítása az aktuális PowerShell-munkamenet további Azure-webhely-helyreállítási műveleteihez való használatra.</span><span class="sxs-lookup"><span data-stu-id="ef417-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="ef417-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef417-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef417-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef417-105">DESCRIPTION</span></span>
<span data-ttu-id="ef417-106">A **set-AzRecoveryServicesAsrVaultContext** parancsmag az Azure webhely-helyreállítási boltozat környezetének beállításával további műveleteket végezhet.</span><span class="sxs-lookup"><span data-stu-id="ef417-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="ef417-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef417-107">EXAMPLES</span></span>

### <span data-ttu-id="ef417-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef417-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="ef417-109">A boltozat környezetének beállítása a megadott helyreállítási szolgáltatások boltozatára az aktuális PowerShell-munkamenetben a további Azure-webhely-helyreállítási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="ef417-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="ef417-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef417-110">PARAMETERS</span></span>

### <span data-ttu-id="ef417-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef417-111">-DefaultProfile</span></span>
<span data-ttu-id="ef417-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef417-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef417-113">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="ef417-113">-Vault</span></span>
<span data-ttu-id="ef417-114">A helyreállítási szolgáltatások Vault-objektuma, amely megfelel a helyreállítási szolgáltatások boltozatának.</span><span class="sxs-lookup"><span data-stu-id="ef417-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="ef417-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef417-115">-Confirm</span></span>
<span data-ttu-id="ef417-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef417-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef417-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef417-117">-WhatIf</span></span>
<span data-ttu-id="ef417-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef417-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef417-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef417-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef417-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef417-120">CommonParameters</span></span>
<span data-ttu-id="ef417-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef417-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef417-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef417-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef417-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef417-123">INPUTS</span></span>

### <span data-ttu-id="ef417-124">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="ef417-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ef417-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef417-125">OUTPUTS</span></span>

### <span data-ttu-id="ef417-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="ef417-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="ef417-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef417-127">NOTES</span></span>

## <span data-ttu-id="ef417-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef417-128">RELATED LINKS</span></span>
