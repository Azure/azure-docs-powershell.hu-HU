---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: 52abb3af83f7ee0d8724243c917e3aeb58592ac9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679099"
---
# <span data-ttu-id="81086-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="81086-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="81086-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81086-102">SYNOPSIS</span></span>
<span data-ttu-id="81086-103">Eltávolítja a virtuális gép biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="81086-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81086-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81086-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81086-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81086-105">DESCRIPTION</span></span>

## <span data-ttu-id="81086-106">Példák</span><span class="sxs-lookup"><span data-stu-id="81086-106">EXAMPLES</span></span>

### <span data-ttu-id="81086-107">1:</span><span class="sxs-lookup"><span data-stu-id="81086-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="81086-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81086-108">PARAMETERS</span></span>

### <span data-ttu-id="81086-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81086-109">-DefaultProfile</span></span>
<span data-ttu-id="81086-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81086-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81086-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81086-111">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81086-112">-Címke</span><span class="sxs-lookup"><span data-stu-id="81086-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81086-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="81086-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81086-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81086-114">CommonParameters</span></span>
<span data-ttu-id="81086-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81086-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81086-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81086-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81086-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81086-117">INPUTS</span></span>

## <span data-ttu-id="81086-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81086-118">OUTPUTS</span></span>

## <span data-ttu-id="81086-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81086-119">NOTES</span></span>

## <span data-ttu-id="81086-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81086-120">RELATED LINKS</span></span>

