---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 3607835496aa6f99cfd2b42383654180d6b12331
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838564"
---
# <span data-ttu-id="e3f55-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e3f55-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="e3f55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3f55-102">SYNOPSIS</span></span>

<span data-ttu-id="e3f55-103">Megnyeri a helyreállítási szolgáltatások boltozatát.</span><span class="sxs-lookup"><span data-stu-id="e3f55-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="e3f55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3f55-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3f55-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3f55-105">DESCRIPTION</span></span>

<span data-ttu-id="e3f55-106">A **Get-AzRecoveryServicesVault** parancsmag az aktuális előfizetésben a helyreállítási szolgáltatások boltozatának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="e3f55-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="e3f55-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e3f55-107">EXAMPLES</span></span>

### <span data-ttu-id="e3f55-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3f55-108">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="e3f55-109">A kijelölt előfizetésben lévő Vault-lista lekérése</span><span class="sxs-lookup"><span data-stu-id="e3f55-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="e3f55-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="e3f55-110">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="e3f55-111">A kijelölt előfizetéshez tartozó Vault-lista lekérése az erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="e3f55-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="e3f55-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="e3f55-112">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="e3f55-113">Adja meg a boltozatot az erőforrás csoportban a megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="e3f55-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="e3f55-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3f55-114">PARAMETERS</span></span>

### <span data-ttu-id="e3f55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f55-115">-DefaultProfile</span></span>

<span data-ttu-id="e3f55-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3f55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f55-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3f55-117">-Name</span></span>

<span data-ttu-id="e3f55-118">A lekérdezni kívánt boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3f55-118">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="e3f55-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f55-119">-ResourceGroupName</span></span>

<span data-ttu-id="e3f55-120">Annak az Azure erőforrás-csoportnak a neve, amelyből a megadott helyreállítási szolgáltatási objektumot be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="e3f55-120">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="e3f55-121">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f55-121">-CommonParameters</span></span>

<span data-ttu-id="e3f55-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3f55-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f55-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e3f55-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f55-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3f55-124">INPUTS</span></span>

### <span data-ttu-id="e3f55-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="e3f55-125">None</span></span>

## <span data-ttu-id="e3f55-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3f55-126">OUTPUTS</span></span>

### <span data-ttu-id="e3f55-127">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e3f55-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e3f55-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3f55-128">NOTES</span></span>

## <span data-ttu-id="e3f55-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3f55-129">RELATED LINKS</span></span>

[<span data-ttu-id="e3f55-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e3f55-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e3f55-131">Új – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e3f55-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="e3f55-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e3f55-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
