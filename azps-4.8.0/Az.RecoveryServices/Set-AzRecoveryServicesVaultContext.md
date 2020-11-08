---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184016"
---
# <span data-ttu-id="e7d54-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="e7d54-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="e7d54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7d54-102">SYNOPSIS</span></span>

<span data-ttu-id="e7d54-103">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="e7d54-103">Sets vault context.</span></span>

## <span data-ttu-id="e7d54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7d54-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7d54-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7d54-105">DESCRIPTION</span></span>

<span data-ttu-id="e7d54-106">A **set-AzRecoveryServicesVaultContext** parancsmag az Azure webhely-helyreállítási szolgáltatások boltozat-környezetét állítja be.</span><span class="sxs-lookup"><span data-stu-id="e7d54-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="e7d54-107">Figyelmeztetés: ezt a parancsmagot egy jövőbeli, megjelenő változtatási kiadásban érvénytelenítjük.</span><span class="sxs-lookup"><span data-stu-id="e7d54-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="e7d54-108">A program nem jeleníti meg a cserét.</span><span class="sxs-lookup"><span data-stu-id="e7d54-108">There will be no replacement for it.</span></span> <span data-ttu-id="e7d54-109">Kérjük, használja a-VaultId paramétert minden helyreállítási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e7d54-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="e7d54-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e7d54-110">EXAMPLES</span></span>

### <span data-ttu-id="e7d54-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7d54-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="e7d54-112">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="e7d54-112">Sets vault context.</span></span>

## <span data-ttu-id="e7d54-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7d54-113">PARAMETERS</span></span>

### <span data-ttu-id="e7d54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d54-114">-DefaultProfile</span></span>

<span data-ttu-id="e7d54-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7d54-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7d54-116">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="e7d54-116">-Vault</span></span>

<span data-ttu-id="e7d54-117">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7d54-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="e7d54-118">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e7d54-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="e7d54-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d54-119">CommonParameters</span></span>
<span data-ttu-id="e7d54-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7d54-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d54-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e7d54-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d54-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7d54-122">INPUTS</span></span>

### <span data-ttu-id="e7d54-123">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e7d54-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e7d54-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7d54-124">OUTPUTS</span></span>

### <span data-ttu-id="e7d54-125">System. Void</span><span class="sxs-lookup"><span data-stu-id="e7d54-125">System.Void</span></span>

## <span data-ttu-id="e7d54-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7d54-126">NOTES</span></span>

## <span data-ttu-id="e7d54-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7d54-127">RELATED LINKS</span></span>
