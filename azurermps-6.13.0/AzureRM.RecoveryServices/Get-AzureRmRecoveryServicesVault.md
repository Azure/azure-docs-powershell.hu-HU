---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 0812fc8aa5673f6475fb822137cffff025003d32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680626"
---
# <span data-ttu-id="4ec93-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ec93-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="4ec93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ec93-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec93-103">Megnyeri a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="4ec93-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ec93-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ec93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ec93-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec93-106">A **Get-AzureRmRecoveryServicesVault** parancsmag az aktuális előfizetésben a helyreállítási szolgáltatások boltozatának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="4ec93-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="4ec93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ec93-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec93-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ec93-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="4ec93-109">A kijelölt előfizetésben lévő Vault-lista lekérése</span><span class="sxs-lookup"><span data-stu-id="4ec93-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="4ec93-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="4ec93-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="4ec93-111">A kijelölt előfizetéshez tartozó Vault-lista lekérése az erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="4ec93-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="4ec93-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="4ec93-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="4ec93-113">Adja meg a boltozatot az erőforrás csoportban a megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="4ec93-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="4ec93-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ec93-114">PARAMETERS</span></span>

### <span data-ttu-id="4ec93-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ec93-115">-Name</span></span>
<span data-ttu-id="4ec93-116">A lekérdezni kívánt boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ec93-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec93-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec93-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ec93-118">Annak az Azure-erőforrás csoportnak a nevét adja meg, amelyből a megadott helyreállítási szolgáltatások objektumát szeretné létrehozni vagy onnan beolvasni.</span><span class="sxs-lookup"><span data-stu-id="4ec93-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec93-119">-DefaultProfile</span></span>
<span data-ttu-id="4ec93-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ec93-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ec93-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec93-121">CommonParameters</span></span>
<span data-ttu-id="4ec93-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ec93-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec93-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec93-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec93-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ec93-124">INPUTS</span></span>

### <span data-ttu-id="4ec93-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="4ec93-125">None</span></span>

## <span data-ttu-id="4ec93-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ec93-126">OUTPUTS</span></span>

### <span data-ttu-id="4ec93-127">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="4ec93-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4ec93-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ec93-128">NOTES</span></span>

## <span data-ttu-id="4ec93-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ec93-129">RELATED LINKS</span></span>

[<span data-ttu-id="4ec93-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4ec93-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="4ec93-131">Új – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ec93-131">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="4ec93-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4ec93-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


