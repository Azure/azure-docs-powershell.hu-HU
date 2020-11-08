---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013541"
---
# <span data-ttu-id="9dcf5-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9dcf5-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="9dcf5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dcf5-102">SYNOPSIS</span></span>
<span data-ttu-id="9dcf5-103">Törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="9dcf5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dcf5-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dcf5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dcf5-105">DESCRIPTION</span></span>
<span data-ttu-id="9dcf5-106">A **Remove-AzRecoveryServicesVault** parancsmag törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="9dcf5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9dcf5-107">EXAMPLES</span></span>

### <span data-ttu-id="9dcf5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9dcf5-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="9dcf5-109">Törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="9dcf5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dcf5-110">PARAMETERS</span></span>

### <span data-ttu-id="9dcf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dcf5-111">-DefaultProfile</span></span>
<span data-ttu-id="9dcf5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dcf5-113">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="9dcf5-113">-Vault</span></span>
<span data-ttu-id="9dcf5-114">Az Azure webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="9dcf5-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9dcf5-115">-Confirm</span></span>
<span data-ttu-id="9dcf5-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dcf5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dcf5-117">-WhatIf</span></span>
<span data-ttu-id="9dcf5-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dcf5-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dcf5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dcf5-120">CommonParameters</span></span>
<span data-ttu-id="9dcf5-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dcf5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dcf5-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9dcf5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dcf5-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dcf5-123">INPUTS</span></span>

### <span data-ttu-id="9dcf5-124">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="9dcf5-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9dcf5-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dcf5-125">OUTPUTS</span></span>

### <span data-ttu-id="9dcf5-126">Microsoft. Azure. Command. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="9dcf5-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="9dcf5-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dcf5-127">NOTES</span></span>

## <span data-ttu-id="9dcf5-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dcf5-128">RELATED LINKS</span></span>

[<span data-ttu-id="9dcf5-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9dcf5-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="9dcf5-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9dcf5-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="9dcf5-131">Új – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9dcf5-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


