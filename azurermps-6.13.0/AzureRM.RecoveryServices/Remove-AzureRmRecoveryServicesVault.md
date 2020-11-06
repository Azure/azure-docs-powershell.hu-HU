---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: e6ac59a84e4244cb6d6815f8e3256618cccd661c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503431"
---
# <span data-ttu-id="0f900-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0f900-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="0f900-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f900-102">SYNOPSIS</span></span>
<span data-ttu-id="0f900-103">Törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="0f900-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f900-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f900-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f900-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f900-105">DESCRIPTION</span></span>
<span data-ttu-id="0f900-106">A **Remove-AzureRmRecoveryServicesVault** parancsmag törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="0f900-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="0f900-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f900-107">EXAMPLES</span></span>

### <span data-ttu-id="0f900-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0f900-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="0f900-109">Törli a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="0f900-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="0f900-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f900-110">PARAMETERS</span></span>

### <span data-ttu-id="0f900-111">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="0f900-111">-Vault</span></span>
<span data-ttu-id="0f900-112">Az Azure webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f900-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="0f900-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f900-113">-Confirm</span></span>
<span data-ttu-id="0f900-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f900-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f900-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f900-115">-WhatIf</span></span>
<span data-ttu-id="0f900-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f900-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f900-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f900-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f900-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f900-118">-DefaultProfile</span></span>
<span data-ttu-id="0f900-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f900-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f900-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f900-120">CommonParameters</span></span>
<span data-ttu-id="0f900-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f900-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f900-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f900-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f900-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f900-123">INPUTS</span></span>

### <span data-ttu-id="0f900-124">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="0f900-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="0f900-125">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f900-125">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="0f900-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f900-126">OUTPUTS</span></span>

### <span data-ttu-id="0f900-127">Microsoft. Azure. Command. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="0f900-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="0f900-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f900-128">NOTES</span></span>

## <span data-ttu-id="0f900-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f900-129">RELATED LINKS</span></span>

[<span data-ttu-id="0f900-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0f900-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="0f900-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0f900-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="0f900-132">Új – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0f900-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

