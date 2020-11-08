---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013523"
---
# <span data-ttu-id="07cea-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="07cea-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="07cea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07cea-102">SYNOPSIS</span></span>

<span data-ttu-id="07cea-103">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="07cea-103">Sets vault context.</span></span>

## <span data-ttu-id="07cea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07cea-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07cea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="07cea-105">DESCRIPTION</span></span>

<span data-ttu-id="07cea-106">A **set-AzRecoveryServicesVaultContext** parancsmag az Azure webhely-helyreállítási szolgáltatások boltozat-környezetét állítja be.</span><span class="sxs-lookup"><span data-stu-id="07cea-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="07cea-107">Figyelmeztetés: ezt a parancsmagot egy jövőbeli, megjelenő változtatási kiadásban érvénytelenítjük.</span><span class="sxs-lookup"><span data-stu-id="07cea-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="07cea-108">A program nem jeleníti meg a cserét.</span><span class="sxs-lookup"><span data-stu-id="07cea-108">There will be no replacement for it.</span></span> <span data-ttu-id="07cea-109">Kérjük, használja a-VaultId paramétert minden helyreállítási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="07cea-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="07cea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="07cea-110">EXAMPLES</span></span>

### <span data-ttu-id="07cea-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07cea-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="07cea-112">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="07cea-112">Sets vault context.</span></span>

## <span data-ttu-id="07cea-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07cea-113">PARAMETERS</span></span>

### <span data-ttu-id="07cea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cea-114">-DefaultProfile</span></span>

<span data-ttu-id="07cea-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07cea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07cea-116">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="07cea-116">-Vault</span></span>

<span data-ttu-id="07cea-117">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07cea-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="07cea-118">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="07cea-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="07cea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cea-119">CommonParameters</span></span>
<span data-ttu-id="07cea-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07cea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cea-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07cea-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cea-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07cea-122">INPUTS</span></span>

### <span data-ttu-id="07cea-123">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="07cea-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="07cea-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07cea-124">OUTPUTS</span></span>

### <span data-ttu-id="07cea-125">System. Void</span><span class="sxs-lookup"><span data-stu-id="07cea-125">System.Void</span></span>

## <span data-ttu-id="07cea-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07cea-126">NOTES</span></span>

## <span data-ttu-id="07cea-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07cea-127">RELATED LINKS</span></span>
