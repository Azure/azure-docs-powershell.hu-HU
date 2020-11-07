---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 410d78df47a37daa90213056170c86f24c423986
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838534"
---
# <span data-ttu-id="bc6c5-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bc6c5-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="bc6c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6c5-103">Windows-kiszolgáló vagy más tároló regisztrációjának megszüntetése a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="bc6c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc6c5-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc6c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6c5-106">A **unregister-AzRecoveryServicesBackupContainer** parancsmag a Windows Server vagy más biztonsági tárolók nyilvántartását a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="bc6c5-107">Ez a parancsmag eltávolítja a tárolóra mutató hivatkozást a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="bc6c5-108">A tároló törlése előtt törölnie kell az adott tárolóhoz társított összes védett adatot.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="bc6c5-109">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bc6c5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bc6c5-110">EXAMPLES</span></span>

### <span data-ttu-id="bc6c5-111">1. példa: Windows-kiszolgáló regisztrációjának megszüntetése a boltozatról</span><span class="sxs-lookup"><span data-stu-id="bc6c5-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="bc6c5-112">Az első parancs beolvassa a server01.contoso.com nevű Windows-tárolót, amely a boltozatban van regisztrálva, majd a $Cont változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="bc6c5-113">A második parancs az Azure Backup Vault-ról regisztrálja a megadott Windows Servert.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="bc6c5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc6c5-114">PARAMETERS</span></span>

### <span data-ttu-id="bc6c5-115">-Container</span><span class="sxs-lookup"><span data-stu-id="bc6c5-115">-Container</span></span>
<span data-ttu-id="bc6c5-116">Egy tartalék tároló objektumot ad meg a regisztráció törléséhez.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="bc6c5-117">**BackupContainer** objektum beolvasásához használja az Get-AzRecoveryServicesBackupContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-117">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc6c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6c5-118">-DefaultProfile</span></span>
<span data-ttu-id="bc6c5-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc6c5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc6c5-120">-PassThru</span></span>
<span data-ttu-id="bc6c5-121">Adja vissza a törlendő tárolót.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-121">Return the container to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc6c5-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bc6c5-122">-VaultId</span></span>
<span data-ttu-id="bc6c5-123">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="bc6c5-123">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc6c5-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc6c5-124">-Confirm</span></span>
<span data-ttu-id="bc6c5-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc6c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc6c5-126">-WhatIf</span></span>
<span data-ttu-id="bc6c5-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc6c5-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc6c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6c5-129">CommonParameters</span></span>
<span data-ttu-id="bc6c5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc6c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6c5-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc6c5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6c5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc6c5-132">INPUTS</span></span>

### <span data-ttu-id="bc6c5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bc6c5-133">System.String</span></span>

## <span data-ttu-id="bc6c5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc6c5-134">OUTPUTS</span></span>

### <span data-ttu-id="bc6c5-135">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="bc6c5-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="bc6c5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc6c5-136">NOTES</span></span>

## <span data-ttu-id="bc6c5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc6c5-137">RELATED LINKS</span></span>

[<span data-ttu-id="bc6c5-138">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bc6c5-138">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


