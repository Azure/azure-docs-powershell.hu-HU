---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 9329f35377731eeb3e59e01a673129b5505abf49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678954"
---
# <span data-ttu-id="f4618-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="f4618-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="f4618-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4618-102">SYNOPSIS</span></span>
<span data-ttu-id="f4618-103">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="f4618-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4618-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4618-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4618-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4618-105">DESCRIPTION</span></span>
<span data-ttu-id="f4618-106">A **set-AzureRmRecoveryServicesVaultContext** parancsmag az Azure webhely-helyreállítási szolgáltatások boltozat-környezetét állítja be.</span><span class="sxs-lookup"><span data-stu-id="f4618-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="f4618-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4618-107">EXAMPLES</span></span>

### <span data-ttu-id="f4618-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4618-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="f4618-109">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="f4618-109">Sets vault context.</span></span>

## <span data-ttu-id="f4618-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4618-110">PARAMETERS</span></span>

### <span data-ttu-id="f4618-111">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="f4618-111">-Vault</span></span>
<span data-ttu-id="f4618-112">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4618-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="f4618-113">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f4618-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="f4618-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4618-114">-DefaultProfile</span></span>
<span data-ttu-id="f4618-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4618-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4618-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4618-116">CommonParameters</span></span>
<span data-ttu-id="f4618-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4618-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4618-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4618-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4618-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4618-119">INPUTS</span></span>

### <span data-ttu-id="f4618-120">ARSVault</span><span class="sxs-lookup"><span data-stu-id="f4618-120">ARSVault</span></span>
<span data-ttu-id="f4618-121">A "Vault" paraméter az "ARSVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f4618-121">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="f4618-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4618-122">OUTPUTS</span></span>

## <span data-ttu-id="f4618-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4618-123">NOTES</span></span>

## <span data-ttu-id="f4618-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4618-124">RELATED LINKS</span></span>

