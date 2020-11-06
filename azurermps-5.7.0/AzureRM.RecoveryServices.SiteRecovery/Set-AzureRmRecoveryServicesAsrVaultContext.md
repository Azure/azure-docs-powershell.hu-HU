---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: c85d372ccd17b23fec46655245d050b668a32dc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495295"
---
# <span data-ttu-id="518df-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="518df-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="518df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="518df-102">SYNOPSIS</span></span>
<span data-ttu-id="518df-103">A helyreállítási szolgáltatások Vault-környezetének beállítása az aktuális PowerShell-munkamenet további Azure-webhely-helyreállítási műveleteihez való használatra.</span><span class="sxs-lookup"><span data-stu-id="518df-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="518df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="518df-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="518df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="518df-105">DESCRIPTION</span></span>
<span data-ttu-id="518df-106">A **set-AzureRmRecoveryServicesAsrVaultContext** parancsmag az Azure webhely-helyreállítási boltozat környezetének beállításával további műveleteket végezhet.</span><span class="sxs-lookup"><span data-stu-id="518df-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="518df-107">Példák</span><span class="sxs-lookup"><span data-stu-id="518df-107">EXAMPLES</span></span>

### <span data-ttu-id="518df-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="518df-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="518df-109">A boltozat környezetének beállítása a megadott helyreállítási szolgáltatások boltozatára az aktuális PowerShell-munkamenetben a további Azure-webhely-helyreállítási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="518df-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="518df-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="518df-110">PARAMETERS</span></span>

### <span data-ttu-id="518df-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="518df-111">-Confirm</span></span>
<span data-ttu-id="518df-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="518df-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="518df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="518df-113">-DefaultProfile</span></span>
<span data-ttu-id="518df-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="518df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="518df-115">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="518df-115">-Vault</span></span>
<span data-ttu-id="518df-116">A helyreállítási szolgáltatások Vault-objektuma, amely megfelel a helyreállítási szolgáltatások boltozatának.</span><span class="sxs-lookup"><span data-stu-id="518df-116">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="518df-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="518df-117">-WhatIf</span></span>
<span data-ttu-id="518df-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="518df-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="518df-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="518df-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="518df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="518df-120">CommonParameters</span></span>
<span data-ttu-id="518df-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="518df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="518df-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="518df-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="518df-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="518df-123">INPUTS</span></span>

### <span data-ttu-id="518df-124">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="518df-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="518df-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="518df-125">OUTPUTS</span></span>

### <span data-ttu-id="518df-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="518df-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="518df-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="518df-127">NOTES</span></span>

## <span data-ttu-id="518df-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="518df-128">RELATED LINKS</span></span>
