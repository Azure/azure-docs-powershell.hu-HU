---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679350"
---
# <span data-ttu-id="7a655-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7a655-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="7a655-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a655-102">SYNOPSIS</span></span>
<span data-ttu-id="7a655-103">Törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="7a655-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a655-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a655-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a655-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a655-105">DESCRIPTION</span></span>
<span data-ttu-id="7a655-106">A **Remove-AzureRmRecoveryServicesVault** parancsmag törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="7a655-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="7a655-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a655-107">EXAMPLES</span></span>

## <span data-ttu-id="7a655-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a655-108">PARAMETERS</span></span>

### <span data-ttu-id="7a655-109">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="7a655-109">-Vault</span></span>
<span data-ttu-id="7a655-110">Az Azure webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a655-110">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="7a655-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a655-111">-Confirm</span></span>
<span data-ttu-id="7a655-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a655-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a655-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a655-113">-WhatIf</span></span>
<span data-ttu-id="7a655-114">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a655-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a655-115">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a655-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a655-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a655-116">-DefaultProfile</span></span>
<span data-ttu-id="7a655-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a655-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a655-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a655-118">CommonParameters</span></span>
<span data-ttu-id="7a655-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a655-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a655-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a655-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a655-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a655-121">INPUTS</span></span>

### <span data-ttu-id="7a655-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="7a655-122">ARSVault</span></span>
<span data-ttu-id="7a655-123">A "Vault" paraméter az "ARSVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7a655-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="7a655-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a655-124">OUTPUTS</span></span>

### <span data-ttu-id="7a655-125">Microsoft. Azure. Command. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="7a655-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="7a655-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a655-126">NOTES</span></span>

## <span data-ttu-id="7a655-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a655-127">RELATED LINKS</span></span>

[<span data-ttu-id="7a655-128">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7a655-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7a655-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7a655-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7a655-130">Új – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7a655-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


