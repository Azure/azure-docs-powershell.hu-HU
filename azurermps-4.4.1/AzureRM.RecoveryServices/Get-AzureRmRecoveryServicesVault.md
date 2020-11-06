---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501656"
---
# <span data-ttu-id="ef600-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef600-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="ef600-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef600-102">SYNOPSIS</span></span>
<span data-ttu-id="ef600-103">Megnyeri a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="ef600-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef600-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef600-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef600-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef600-105">DESCRIPTION</span></span>
<span data-ttu-id="ef600-106">A **Get-AzureRmRecoveryServicesVault** parancsmag az aktuális előfizetésben a helyreállítási szolgáltatások boltozatának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="ef600-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="ef600-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef600-107">EXAMPLES</span></span>

## <span data-ttu-id="ef600-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef600-108">PARAMETERS</span></span>

### <span data-ttu-id="ef600-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef600-109">-Name</span></span>
<span data-ttu-id="ef600-110">A lekérdezni kívánt boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef600-110">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef600-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef600-111">-ResourceGroupName</span></span>
<span data-ttu-id="ef600-112">Annak az Azure-erőforrás csoportnak a nevét adja meg, amelyből a megadott helyreállítási szolgáltatások objektumát szeretné létrehozni vagy onnan beolvasni.</span><span class="sxs-lookup"><span data-stu-id="ef600-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef600-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef600-113">-DefaultProfile</span></span>
<span data-ttu-id="ef600-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef600-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef600-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef600-115">CommonParameters</span></span>
<span data-ttu-id="ef600-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef600-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef600-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef600-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef600-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef600-118">INPUTS</span></span>

## <span data-ttu-id="ef600-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef600-119">OUTPUTS</span></span>

### <span data-ttu-id="ef600-120">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="ef600-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="ef600-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef600-121">NOTES</span></span>

## <span data-ttu-id="ef600-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef600-122">RELATED LINKS</span></span>

[<span data-ttu-id="ef600-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ef600-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ef600-124">Új – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef600-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="ef600-125">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef600-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


