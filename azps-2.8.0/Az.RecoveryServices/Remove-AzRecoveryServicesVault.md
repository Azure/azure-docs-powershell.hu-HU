---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: a0f21fc8cde4c64eaf1e8ea27bf05eff8d664c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838541"
---
# <span data-ttu-id="18f84-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="18f84-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="18f84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18f84-102">SYNOPSIS</span></span>
<span data-ttu-id="18f84-103">Törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="18f84-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="18f84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18f84-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18f84-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18f84-105">DESCRIPTION</span></span>
<span data-ttu-id="18f84-106">A **Remove-AzRecoveryServicesVault** parancsmag törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="18f84-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="18f84-107">Példák</span><span class="sxs-lookup"><span data-stu-id="18f84-107">EXAMPLES</span></span>

### <span data-ttu-id="18f84-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="18f84-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="18f84-109">Törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="18f84-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="18f84-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18f84-110">PARAMETERS</span></span>

### <span data-ttu-id="18f84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f84-111">-DefaultProfile</span></span>
<span data-ttu-id="18f84-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18f84-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18f84-113">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="18f84-113">-Vault</span></span>
<span data-ttu-id="18f84-114">Az Azure webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18f84-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="18f84-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18f84-115">-Confirm</span></span>
<span data-ttu-id="18f84-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18f84-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18f84-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18f84-117">-WhatIf</span></span>
<span data-ttu-id="18f84-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="18f84-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18f84-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18f84-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18f84-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f84-120">CommonParameters</span></span>
<span data-ttu-id="18f84-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18f84-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f84-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f84-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f84-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18f84-123">INPUTS</span></span>

### <span data-ttu-id="18f84-124">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="18f84-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="18f84-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18f84-125">OUTPUTS</span></span>

### <span data-ttu-id="18f84-126">Microsoft. Azure. Command. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="18f84-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="18f84-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18f84-127">NOTES</span></span>

## <span data-ttu-id="18f84-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18f84-128">RELATED LINKS</span></span>

[<span data-ttu-id="18f84-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="18f84-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="18f84-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="18f84-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="18f84-131">Új – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="18f84-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


