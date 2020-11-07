---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669604"
---
# <span data-ttu-id="1a1b4-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="1a1b4-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="1a1b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1b4-103">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="1a1b4-103">Sets vault context.</span></span>

## <span data-ttu-id="1a1b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a1b4-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a1b4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a1b4-105">DESCRIPTION</span></span>
<span data-ttu-id="1a1b4-106">A **set-AzRecoveryServicesVaultContext** parancsmag az Azure webhely-helyreállítási szolgáltatások boltozat-környezetét állítja be.</span><span class="sxs-lookup"><span data-stu-id="1a1b4-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="1a1b4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1a1b4-107">EXAMPLES</span></span>

### <span data-ttu-id="1a1b4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1a1b4-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="1a1b4-109">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="1a1b4-109">Sets vault context.</span></span>

## <span data-ttu-id="1a1b4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a1b4-110">PARAMETERS</span></span>

### <span data-ttu-id="1a1b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1b4-111">-DefaultProfile</span></span>
<span data-ttu-id="1a1b4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a1b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a1b4-113">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="1a1b4-113">-Vault</span></span>
<span data-ttu-id="1a1b4-114">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a1b4-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="1a1b4-115">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1a1b4-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="1a1b4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1b4-116">CommonParameters</span></span>
<span data-ttu-id="1a1b4-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a1b4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1b4-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a1b4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1b4-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a1b4-119">INPUTS</span></span>

### <span data-ttu-id="1a1b4-120">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="1a1b4-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="1a1b4-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a1b4-121">OUTPUTS</span></span>

### <span data-ttu-id="1a1b4-122">System. Void</span><span class="sxs-lookup"><span data-stu-id="1a1b4-122">System.Void</span></span>

## <span data-ttu-id="1a1b4-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a1b4-123">NOTES</span></span>

## <span data-ttu-id="1a1b4-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a1b4-124">RELATED LINKS</span></span>