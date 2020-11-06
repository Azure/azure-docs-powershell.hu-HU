---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 08166ea1ebe4c78521a68f9e5423a7947e78b699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503432"
---
# <span data-ttu-id="16ebd-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="16ebd-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="16ebd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="16ebd-103">Új helyreállítási szolgáltatások boltozatának létrehozása</span><span class="sxs-lookup"><span data-stu-id="16ebd-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16ebd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16ebd-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ebd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16ebd-105">DESCRIPTION</span></span>
<span data-ttu-id="16ebd-106">A **New-AzureRmRecoveryServicesVault** parancsmag új helyreállítási szolgáltatások boltozatát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="16ebd-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="16ebd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="16ebd-107">EXAMPLES</span></span>

### <span data-ttu-id="16ebd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="16ebd-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="16ebd-109">Helyreállítási szolgáltatás boltozatának létrehozása az erőforrás csoportban és az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="16ebd-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="16ebd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16ebd-110">PARAMETERS</span></span>

### <span data-ttu-id="16ebd-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="16ebd-111">-Location</span></span>
<span data-ttu-id="16ebd-112">A boltozat földrajzi helyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16ebd-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ebd-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="16ebd-113">-Name</span></span>
<span data-ttu-id="16ebd-114">A létrehozandó boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16ebd-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ebd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ebd-115">-ResourceGroupName</span></span>
<span data-ttu-id="16ebd-116">Annak az Azure-erőforrás csoportnak a nevét adja meg, amelyből a megadott helyreállítási szolgáltatások objektumát szeretné létrehozni vagy onnan beolvasni.</span><span class="sxs-lookup"><span data-stu-id="16ebd-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ebd-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="16ebd-117">-Confirm</span></span>
<span data-ttu-id="16ebd-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="16ebd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ebd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ebd-119">-WhatIf</span></span>
<span data-ttu-id="16ebd-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="16ebd-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16ebd-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16ebd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ebd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ebd-122">-DefaultProfile</span></span>
<span data-ttu-id="16ebd-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16ebd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ebd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ebd-124">CommonParameters</span></span>
<span data-ttu-id="16ebd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16ebd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ebd-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ebd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ebd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16ebd-127">INPUTS</span></span>

### <span data-ttu-id="16ebd-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="16ebd-128">None</span></span>

## <span data-ttu-id="16ebd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16ebd-129">OUTPUTS</span></span>

### <span data-ttu-id="16ebd-130">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="16ebd-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="16ebd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16ebd-131">NOTES</span></span>

## <span data-ttu-id="16ebd-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16ebd-132">RELATED LINKS</span></span>

[<span data-ttu-id="16ebd-133">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="16ebd-133">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="16ebd-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="16ebd-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="16ebd-135">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="16ebd-135">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


