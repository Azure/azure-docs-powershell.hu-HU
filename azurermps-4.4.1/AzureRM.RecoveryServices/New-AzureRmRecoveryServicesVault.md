---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493390"
---
# <span data-ttu-id="7d073-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7d073-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="7d073-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d073-102">SYNOPSIS</span></span>
<span data-ttu-id="7d073-103">Új helyreállítási szolgáltatások boltozatának létrehozása</span><span class="sxs-lookup"><span data-stu-id="7d073-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d073-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d073-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d073-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d073-105">DESCRIPTION</span></span>
<span data-ttu-id="7d073-106">A **New-AzureRmRecoveryServicesVault** parancsmag új helyreállítási szolgáltatások boltozatát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7d073-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="7d073-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7d073-107">EXAMPLES</span></span>

## <span data-ttu-id="7d073-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d073-108">PARAMETERS</span></span>

### <span data-ttu-id="7d073-109">-Hely</span><span class="sxs-lookup"><span data-stu-id="7d073-109">-Location</span></span>
<span data-ttu-id="7d073-110">A boltozat földrajzi helyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d073-110">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d073-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d073-111">-Name</span></span>
<span data-ttu-id="7d073-112">A létrehozandó boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d073-112">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d073-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d073-113">-ResourceGroupName</span></span>
<span data-ttu-id="7d073-114">Annak az Azure-erőforrás csoportnak a nevét adja meg, amelyből a megadott helyreállítási szolgáltatások objektumát szeretné létrehozni vagy onnan beolvasni.</span><span class="sxs-lookup"><span data-stu-id="7d073-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d073-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d073-115">-Confirm</span></span>
<span data-ttu-id="7d073-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d073-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d073-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d073-117">-WhatIf</span></span>
<span data-ttu-id="7d073-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d073-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d073-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d073-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d073-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d073-120">-DefaultProfile</span></span>
<span data-ttu-id="7d073-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d073-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d073-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d073-122">CommonParameters</span></span>
<span data-ttu-id="7d073-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d073-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d073-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d073-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d073-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d073-125">INPUTS</span></span>

## <span data-ttu-id="7d073-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d073-126">OUTPUTS</span></span>

### <span data-ttu-id="7d073-127">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="7d073-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7d073-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d073-128">NOTES</span></span>

## <span data-ttu-id="7d073-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d073-129">RELATED LINKS</span></span>

[<span data-ttu-id="7d073-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7d073-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7d073-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7d073-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7d073-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7d073-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


